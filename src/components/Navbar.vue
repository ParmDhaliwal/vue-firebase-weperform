<template>
	<nav>
		<v-toolbar flat app>
<!--			<v-toolbar-side-icon class="grey&#45;&#45;text" @click="drawer = !drawer"></v-toolbar-side-icon>-->
			<v-toolbar-title class="text-uppercase grey--text pr-3">
				<span class="font-weight-light"><router-link to="/">We</router-link></span>
				<span><router-link to="/">Perform</router-link></span>
			</v-toolbar-title>
      <v-toolbar-items class="hidden-sm-and-down">
        <v-btn v-if="user" flat color="grey" to="/performers">Search
          <v-icon right small>search</v-icon>
        </v-btn>
        <v-btn v-if="user" flat color="grey" to="/bookings">Bookings
          <v-badge>
            <v-icon right small>shopping_cart</v-icon>
            <span slot="badge">{{ count }}</span>
          </v-badge>
        </v-btn>
      </v-toolbar-items>

        <v-spacer></v-spacer>
      <v-toolbar-items>
        <v-btn v-if="user" flat color="grey" to="/profile">Profile
          <v-icon right small>face</v-icon>
        </v-btn>
        <Signout v-if="user"/>
        <PopupRegister v-if="user === null"/>
        <PopupLogin v-if="user === null"/>
      </v-toolbar-items>
		</v-toolbar>
	</nav>
</template>

<script>
	import PopupRegister from '../views/PopupRegister';
	import PopupLogin from '../views/PopupLogin';
  import Signout from '../views/Signout';
  import { mapState } from 'vuex';

	export default {
		components: { PopupRegister, PopupLogin, Signout },
		data() {
			return {
				drawer: false,
				links: [
					{ icon: 'home', text: 'Home', route: '/' },
					{ icon: 'info', text: 'About', route: '/about' },
					{ icon: 'list', text: 'User List', route: '/admin' },
					{ icon: 'people', text: 'Performers', route: '/performers' },
					{ icon: 'shopping_cart', text: 'Bookings', route: '/bookings' }
				]
			}
		},
    computed: mapState([
      'user',
      'count'
    ]),
    methods: {
    }
	}
</script>

<style scoped>
	a {
		text-decoration: none;
		color: grey;
	}
</style>
