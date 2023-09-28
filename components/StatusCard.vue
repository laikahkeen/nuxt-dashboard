<template>
	<section class="grid gap-5 md:grid-cols-2">
		<!-- revenue card -->
		<div class="rounded-lg border bg-card p-6">
			<div class="flex items-center justify-between">
				<p class="text-sm font-medium">Total Revenue</p>
				<span class="shrink-0">
					<Icon name="heroicons:banknotes" class="w-4h4 text-muted-foreground" />
				</span>
			</div>
			<p class="mt-1.5 text-xl font-extrabold">$432,156,54</p>
			<p class="text-xs text-muted-foreground">20% more than last month</p>
		</div>
		<!-- sales card -->
		<div class="rounded-lg border bg-card p-6">
			<div class="flex items-center justify-between">
				<p class="text-sm font-medium">Total Sales</p>
				<span class="shrink-0">
					<Icon name="heroicons:credit-card" class="w-4h4 text-muted-foreground" />
				</span>
			</div>
			<p class="mt-1.5 text-xl font-extrabold">$32,156,54</p>
			<p class="text-xs text-muted-foreground">13.2% more than last month</p>
		</div>
	</section>
</template>

<script setup></script>

<style></style>
