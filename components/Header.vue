<template>
	<header class="sticky top-0 z-20 border-b bg-background/80 backdrop-blur">
		<!-- flex cotainer -->
		<div class="container flex h-16 items-center justify-between">
			<!-- left side header -->
			<div class="flex items-center gap-3">
				<!-- logo -->
				<img src="/icon.svg" alt="Analytics Logo" class="h-7 w-7 object-contain" />
				<!-- page title -->
				<NuxtLink to="/" class="text-xl font-bold">Analytics</NuxtLink>
			</div>
			<!-- right side header -->
			<div class="flex items-center gap-5">
				<!-- color theme toggle -->
				<button class="flex h-9 w-9 shrink-0 items-center justify-center rounded-full border bg-background" @click="toggleTheme">
					<Icon name="heroicons:sun" class="h-5 w-5" />
				</button>
				<!-- profile dropdown menu -->
				<HMenu as="div" class="relative">
					<HMenuButton class="flex h-9 w-9 shrink-0 items-center justify-center rounded-full border bg-background">
						<img src="https://randomuser.me/api/portraits/med/men/75.jpg" alt="logged in user" class="w-full h-full rounded-full" />
					</HMenuButton>

					<TransitionScale :scale="0.8" origin="top right">
						<HMenuItems class="absolute right-0 z-10 mt-3 w-48 rounded-md border bg-background focus:outline-none focus-visible:ring-2 focus-visible:ring-ring">
							<div class="border-b px-3 py-1.5 text-sm">
								<p class="font-semibold">Hello John</p>
								<a href="mailto:johndoe@test.com" class="leading-none text-muted-foreground">johndoe@test.com</a>
							</div>
							<div class="p-1">
								<template v-for="(p, i) in profileMenuOptions" :key="i">
									<HMenuItem v-if="!p.divider" v-slot="{ active }">
										<button :class="[active && 'bg-muted']" class="inline-flex w-full items-center rounded-md p-2 text-sm font-medium">
											{{ p.title }}
										</button>
									</HMenuItem>
									<hr v-else />
								</template>
							</div>
						</HMenuItems>
					</TransitionScale>
				</HMenu>
			</div>
		</div>
	</header>
</template>

<script setup>
const mode = useColorMode();
const toggleTheme = () => {
	mode.value = mode.value === "light" ? "dark" : "light";
};

const profileMenuOptions = [{ title: "Profile" }, { title: "Billing" }, { title: "Settings" }, { title: "Team members" }, { title: "Sales" }, { divider: true }, { title: "Logout" }];
</script>

<style scoped></style>
