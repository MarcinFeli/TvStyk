<template>
	<nav>
		<v-app-bar app color="dark" dark>
			<v-container style="max-width: 1200px; position: relative" class="d-flex align-center p0-a">
				<v-app-bar-nav-icon class="hidden-lg-and-up" @click="drawer = !drawer"></v-app-bar-nav-icon>
				<v-btn @click="home" target="_blank" text x-large>
					<v-img
						alt="Vuetify Logo"
						class="shrink mr-2"
						contain
						src="../assets/img/cropped-ikona.png"
						transition="scale-transition"
						width="40" />
					Telewizja <span class="lime--text text--lighten-2"> S</span
					><span class="light-blue--text text--lighten-1"> T</span><span class="lime--text text--lighten-2"> Y</span
					><span class="light-blue--text text--lighten-1"> K</span>
				</v-btn>
				<v-spacer></v-spacer>
				<div class="hidden-md-and-down">
					<v-hover v-slot="{ hover }">
						<v-btn @click="scrollAboutUs" target="_blank" text :color="hover ? 'blue' : 'white'"> O nas </v-btn>
					</v-hover>
					<v-hover v-slot="{ hover }">
						<v-btn @click="scrollPrograms" target="_blank" text :color="hover ? 'blue' : 'white'"> Programy </v-btn>
					</v-hover>
					<v-hover v-slot="{ hover }">
						<v-btn @click="scrollAdministartion" target="_blank" text :color="hover ? 'blue' : 'white'"> Zarząd </v-btn>
					</v-hover>
					<v-hover v-slot="{ hover }">
						<v-btn @click="scrollRecruitment" target="_blank" text :color="hover ? 'blue' : 'white'">
							Rekrutacja
						</v-btn>
					</v-hover>
					<v-hover v-slot="{ hover }">
						<v-btn @click="scrollContact" target="_blank" text :color="hover ? 'blue' : 'white'"> Kontakt </v-btn>
					</v-hover>
				</div>
			</v-container>
		</v-app-bar>

		<v-navigation-drawer class="hidden-lg-and-up" app v-model="drawer" temporary>
			<v-list nav dense>
				<v-list-item-group v-model="group">
					<v-list-item @click="home(), (drawer = false)">
						<v-list-item-icon>
							<v-icon>mdi-home</v-icon>
						</v-list-item-icon>
						<v-list-item-title>Strona główna</v-list-item-title>
					</v-list-item>
					<v-list-item @click="scrollAboutUs(), (drawer = false)">
						<v-list-item-icon>
							<v-icon>mdi-account</v-icon>
						</v-list-item-icon>
						<v-list-item-title>O nas</v-list-item-title>
					</v-list-item>
					<v-list-item @click="scrollPrograms(), (drawer = false)">
						<v-list-item-icon>
							<v-icon>mdi-projector-screen</v-icon>
						</v-list-item-icon>
						<v-list-item-title>Programy</v-list-item-title>
					</v-list-item>
					<v-list-item @click="scrollAdministartion(), (drawer = false)">
						<v-list-item-icon>
							<v-icon>mdi-account</v-icon>
						</v-list-item-icon>
						<v-list-item-title>Zarząd</v-list-item-title>
					</v-list-item>
					<v-list-item @click="scrollRecruitment(), (drawer = false)">
						<v-list-item-icon>
							<v-icon>mdi-account-group</v-icon>
						</v-list-item-icon>
						<v-list-item-title>Rekrutacja</v-list-item-title>
					</v-list-item>
					<v-list-item @click="scrollContact(), (drawer = false)">
						<v-list-item-icon>
							<v-icon>mdi-phone</v-icon>
						</v-list-item-icon>
						<v-list-item-title>Kontakt</v-list-item-title>
					</v-list-item>
				</v-list-item-group>
			</v-list>
		</v-navigation-drawer>
	</nav>
</template>
<script>
export default {
	name: 'NavigationBar',

	data() {
		function scrollAboutUs() {
			const aboutUs = document.getElementById('aboutus')
			aboutUs.scrollIntoView({ behavior: 'smooth' })
		}
		function home() {
			const start = document.getElementById('header')
			start.scrollIntoView({ behavior: 'smooth' })
		}
		function scrollPrograms() {
			const programs = document.getElementById('programs')
			programs.scrollIntoView({ behavior: 'smooth' })
		}
		function scrollAdministartion() {
			const admin = document.getElementById('administration')
			admin.scrollIntoView({ behavior: 'smooth' })
		}
		function scrollRecruitment() {
			const recrut = document.getElementById('recruitment')
			recrut.scrollIntoView({ behavior: 'smooth' })
		}
		function scrollContact() {
			const contact = document.getElementById('contact')
			contact.scrollIntoView({ behavior: 'smooth' })
		}
		return {
			home,
			scrollAboutUs,
			scrollPrograms,
			scrollAdministartion,
			scrollRecruitment,
			scrollContact,
			drawer: false,
		}
	},
}
</script>
<style lang="scss">
v-app-bar {
	max-width: 1200px;
}
</style>
