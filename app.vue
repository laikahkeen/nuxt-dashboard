<template>
	<div>
		<!-- header -->
		<Header></Header>
		<!-- body -->
		<div class="container lg:grid lg:grid-cols-12 lg:gap-10">
			<!-- sidebar -->
			<Sidebar class="hidden lg:block lg:col-span-3"></Sidebar>
			<!-- main section -->
			<main class="py-5 lg:col-span-6">
				<!-- status cards -->
				<StatusCard></StatusCard>
				<!-- customer list -->
				<NewCustomers></NewCustomers>
				<!-- sales chart -->
				<SalesChart></SalesChart>
				<!-- recent orders -->
				<RecentOrders></RecentOrders>
			</main>
			<div class="hidden py-5 lg:col-span-3 lg:block">
				<!-- profile info -->
				<ProfileInfo></ProfileInfo>
				<!-- reminder -->
				<Reminder></Reminder>
			</div>
		</div>
	</div>
</template>
