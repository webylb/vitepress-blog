// Comment.vue
<template>
	<div id="gitalk-container"></div>
</template>

<script>
export default {
	name: 'comment',
	mounted() {
		const commentConfig = {
			clientID: 'c6bccd90d050b8194d55',
			clientSecret: 'e501eb9f9882bc8bdea03ae11a5c538464393665',
			repo: 'webylb.github.io',
			owner: 'webylb',
			admin: ['webylb'],
			id: location.pathname.substr(0, 50),
			distractionFreeMode: false,
		}
		const gitalk = new Gitalk(commentConfig)
		gitalk.render('gitalk-container')
	}
}
</script>
