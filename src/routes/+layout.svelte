<script lang="ts">
	import '../app.css';

	let { children } = $props();
</script>

<div class="flex min-h-screen bg-gray-50 font-sans text-gray-800">
	<!-- Sidebar -->
	<aside class="hidden w-64 flex-col border-r border-gray-200 bg-white shadow-sm md:flex">
		<div
			class="flex h-16 items-center justify-center border-b border-gray-100 text-xl font-bold tracking-tight text-blue-600"
		>
			Pulseform
		</div>
		<nav class="flex-1 space-y-1 px-4 py-6 text-sm">
			<a
				href="/dashboard"
				class="block rounded-lg px-3 py-2 text-gray-700 transition hover:bg-blue-100 hover:text-blue-600"
				>Dashboard</a
			>
			<a
				href="/surveys"
				class="block rounded-lg px-3 py-2 text-gray-700 transition hover:bg-blue-100 hover:text-blue-600"
				>Surveys</a
			>
			<a
				href="/analytics"
				class="block rounded-lg px-3 py-2 text-gray-700 transition hover:bg-blue-100 hover:text-blue-600"
				>Analytics</a
			>
		</nav>
	</aside>

	<!-- Main Content -->
	<div class="flex flex-1 flex-col">
		<!-- Navbar -->
		<header
			class="flex h-16 items-center justify-between border-b border-gray-200 bg-white px-6 shadow-sm"
		>
			<div class="text-base font-medium text-gray-700">Dashboard</div>
			<div class="text-sm text-gray-500">
				Logged in as: <span class="font-semibold text-gray-800">admin@example.com</span>
			</div>
		</header>

		<!-- Page Content -->
		<main class="flex-1 overflow-y-auto bg-white p-6">
			{@render children()}
		</main>
	</div>
</div>
