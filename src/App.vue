<template>
  <div id="app">
    <ResponsiveNavigation
		:nav-links="navLinks"
		:image-path="require('./assets/logo.png')"
		background="#fff"
		link-color="#777"
		hoverBackground="#ddd"
    />
    <router-view/>
  </div>
</template>

<script>
import ResponsiveNavigation from '@/components/ResponsiveNavigation'

export default {
  components: {
    ResponsiveNavigation
  },
  data: () => ({
    navLinks: [
      {
        text: 'Contact',
		path: '/contact',
		icon: 'ion-ios-megaphone'
      },
      {
        text: 'About',
		path: '/about',
		icon: 'ion-ios-business'
      },
      {
        text: 'Blog',
		path: '/blog',
		icon: 'ion-ios-bonfire'
      },
      {
        text: 'Portfolio',
		path: '/portfolio',
		icon: 'ion-ios-briefcase'
      }
    ]
  })
}
</script>

<style lang="scss">
@import 'https://unpkg.com/ionicons@4.2.2/dist/css/ionicons.min.css';

figure {
	margin-block-start: 0;
	margin-block-end: 0;
	margin-inline-start: 10px;
	margin-inline-end: 0;
}

body {
  margin: 0;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px;
  a {
    font-weight: bold;
    color: #2c3e50;
    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
