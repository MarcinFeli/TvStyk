<template>
	<section id="administration" class="administration">
		<h1 class="text-h5 text-sm-h4 text font-weight-bold text-center mt-3 mb-3 text-uppercase">
			Nasz zarząd
			<div class="outline"></div>
		</h1>
		<div class="administration__img">
			<div class="administration__shadow"></div>
			<div class="container d-flex align-start flex-wrap">
				<v-hover v-slot="{ hover }">
					<v-card class="mx-auto mb-5" height="auto" width="300">
						<v-img :class="hover ? 'zoom' : ''" src="../assets/img/styk_zarząd_Kamil.jpg" height="auto" cover></v-img>
						<v-card-title class="justify-center"> Kamil Chmiel </v-card-title>
						<v-card-subtitle class="text-center"> Prezez Zarządu Telewizji </v-card-subtitle>
						<v-card-actions>
							<v-btn text @click="show1 = !show1" class="blue--text"> O mnie... </v-btn>
							<v-spacer></v-spacer>
						</v-card-actions>
						<v-expand-transition>
							<div v-show="show1">
								<v-divider></v-divider>
								<v-card-text>
									Student Informatyki na PWr, programista. Swoją przygodę ze Stykiem zaczął w 2016 r. jako montażysta.
									Redaktor naczelnym oraz realizatorem dźwięku. Zainteresowanie TV zaczęło się w liceum, od amatorskiej
									telewizji internetowej założonej ze znajomym.
								</v-card-text>
							</div>
						</v-expand-transition>
					</v-card>
				</v-hover>
				<v-hover v-slot="{ hover }">
					<v-card class="mx-auto mb-5" height="auto" max-width="300">
						<v-img :class="hover ? 'zoom' : ''" src="../assets/img/styk_zarząd_Ewa.jpg" height="auto" cover></v-img>
						<v-card-title class="justify-center"> Ewa Dawidowicz </v-card-title>
						<v-card-subtitle class="text-center"> Redaktor Naczelna </v-card-subtitle>
						<v-card-actions>
							<v-btn text @click="show2 = !show2" class="blue--text"> O mnie... </v-btn>
							<v-spacer></v-spacer>
						</v-card-actions>
						<v-expand-transition>
							<div v-show="show2">
								<v-divider></v-divider>
								<v-card-text>
									Studentka Zarządzania i Inżynierii Produkcji na Wydziale Mechanicznym Politechniki Wrocławskiej.
									Wiecznie uśmiechnięta i pozytywnie zakręcona, ma 1000 pomysłów na minutę. Doskonale czuje się w
									świetle reflektorów i przed kamerą.
								</v-card-text>
							</div>
						</v-expand-transition>
					</v-card>
				</v-hover>
				<v-hover v-slot="{ hover }">
					<v-card class="mx-auto mb-5" height="auto" max-width="300">
						<v-img :class="hover ? 'zoom' : ''" src="../assets/img/styk_zarząd_Adrian.jpg" height="auto" cover></v-img>
						<v-card-title class="justify-center"> Michał Adrjan </v-card-title>
						<v-card-subtitle class="text-center"> Kierownik Techniczny </v-card-subtitle>
						<v-card-actions>
							<v-btn text @click="show3 = !show3" class="blue--text"> O mnie... </v-btn>
							<v-spacer></v-spacer>
						</v-card-actions>
						<v-expand-transition>
							<div v-show="show3">
								<v-divider></v-divider>
								<v-card-text>
									Student Cyberbezpieczeństwa na Wydziale Elektroniki. Kamera to jego narzędzie do kreowania dla widza
									kompletnie innej rzeczywistości. Chce przedstawiać swoją wizję świata za pomocą obrazu.
								</v-card-text>
							</div>
						</v-expand-transition>
					</v-card>
				</v-hover>
				<v-hover v-slot="{ hover }">
					<v-card class="mx-auto" height="auto" max-width="300">
						<v-img :class="hover ? 'zoom' : ''" src="../assets/img/styk_zarząd_Michał.jpg" height="auto" cover></v-img>
						<v-card-title class="justify-center"> Michał Bocian </v-card-title>
						<v-card-subtitle class="text-center"> Kierownik Promocji </v-card-subtitle>
						<v-card-actions>
							<v-btn text @click="show4 = !show4" class="blue--text"> O mnie... </v-btn>
							<v-spacer></v-spacer>
						</v-card-actions>
						<v-expand-transition>
							<div v-show="show4">
								<v-divider></v-divider>
								<v-card-text>
									Absolwent Automatyki i Robotyki, obecnie student Fizyki Technicznej na Politechnice Wrocławskiej.
									Zaczynał dwa lata temu w Styku jako operator. Czuje się dobrze w roli redaktora i montażysty.
								</v-card-text>
							</div>
						</v-expand-transition>
					</v-card>
				</v-hover>
			</div>
		</div>
	</section>
</template>

<script>
export default {
	data: () => ({
		show1: false,
		show2: false,
		show3: false,
		show4: false,
	}),
}
</script>

<style lang="scss">
.v-image {
	.v-image__image {
		transition: all 0.2s;
	}
	&.zoom {
		.v-image__image {
			transform: scale(1.1);
		}
	}
}
.administration {
	scroll-margin: 69px;
	&__img {
		position: relative;
		padding: 20px 0;
		background-image: url('../assets/img/aboutUs.jpg');
		background-attachment: fixed;
		background-size: cover;
		z-index: 1;
	}
	&__shadow {
		position: absolute;
		top: 0;
		height: 100%;
		width: 100%;
		background-color: rgba(0, 0, 0, 0.8);
		z-index: 0;
	}
}
</style>
