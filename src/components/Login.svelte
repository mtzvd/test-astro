<script>
	let user = { loggedIn: false };

	function toggle() {
		user.loggedIn = !user.loggedIn;
	}
</script>

{#if user.loggedIn}
	<button class="button m-1" on:click={toggle}>
		Выйти
	</button>
{/if}

{#if !user.loggedIn}
	<button class="button m-1" on:click={toggle}>
		Войти
	</button>
{/if}