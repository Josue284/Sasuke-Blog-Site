<template>
	<div class="author">

		<g-image alt="Author image" class="author__image" src="https://blog.sasukebot.ml/assets/static/favicon.7b22250.4b12e93ec06b334cdaf96fa6811faff8.png" width="180" height="180" blur="5" />

		<h1 v-if="showTitle" class="author__site-title">
			{{ $static.metadata.siteName }}
		</h1>

		<p class="author__intro">
			Here you can find Official Updates from the Sasuke Bot Development Team.
		</p>

		<p class="author__links">
			<a href="https://sasubot.statuspage.io/">Status</a>
			<a href="https://github.com/Josue284">GitHub</a>
                        <a href="https://discord.com/oauth2/authorize?client_id=629470421724561408&scope=bot+applications.commands&permissions=285599830">Invite</a>
		</p>

	</div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<script>
export default {
	props: ['showTitle']
}
</script>

<style lang="scss">
.author {
	margin: 0 auto;
	max-width: 500px;
	text-align: center;
	padding: calc(var(--space) / 2) 0;

	&__image {
		border-radius: 100%;
		width: 90px;
		height: 90px;
		margin-bottom: 1em;
	}

	&__intro {
		opacity: .8;
	}

	&__site-title {
		font-size: 1.5em;
	}

	&__links {
		margin-top: -.5em;
		a {
			margin: 0 .5em;
		}
	}
}
</style>
