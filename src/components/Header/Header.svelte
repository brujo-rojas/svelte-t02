<script lang="ts">
	import HeaderSandwich from './HeaderSandwich.svelte';
	import HeaderLogo from './HeaderLogo.svelte';
	type HeaderItem = { name: string; href: string };

	export let items: HeaderItem[] = [];

	let itemSelected: HeaderItem | null = null;
	let showMobileMenu = false;

	if (items.length > 0) {
		itemSelected = items[0];
	}
</script>

<header>
	<nav class="Header">
		<div>
			<HeaderLogo />
			<div class="flex items-center lg:order-2">
				<a href="/login" class="btn btn-text">Log in</a>
				<a href="/" class="btn btn-raised--blue">Home</a>
				<HeaderSandwich on:click={() => (showMobileMenu = !showMobileMenu)} />
			</div>
			<div
				class="
				{showMobileMenu ? '' : 'hidden'}
				menu-container"
				id="mobile-menu-2"
			>
				<ul>
					{#each items as item}
						<li>
							<a
								href={item.href}
								class=" {item === itemSelected ? 'is-active' : ''}"
								on:click={() => (itemSelected = item)}>{item.name}</a
							>
						</li>
					{/each}
				</ul>
			</div>
		</div>
	</nav>
</header>
