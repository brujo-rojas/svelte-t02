<script>
	import '../app.scss';
	import Header from '../components/Header/Header.svelte';

	let items = [
		{ name: 'Home', href: '/' },
		{ name: 'Company', href: '/company' },
		{ name: 'Market', href: '/market' },
		{ name: 'Contact', href: '/Contact' }
	];
</script>

<!-- from https://tailwindcomponents.com/component/tailwind-header -->
<Header {items} />

<slot />
