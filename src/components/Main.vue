<template>
  <main>

			<p class="text-white mb-5 text-justify">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Illo doloribus est eligendi voluptates? Quis quia, illum fugiat, optio nobis nihil vero harum accusamus dicta molestias odit dolor ad unde deserunt dignissimos id aliquid eaque ea nesciunt iste impedit, quod ducimus laudantium repellendus! Ad ea, suscipit, iure sit ab, obcaecati quaerat animi eaque molestias quo aut. Provident, recusandae et? Et quod laborum libero nihil. Deserunt optio excepturi molestias ipsum aliquam beatae nulla itaque vel a minus dicta necessitatibus non, explicabo possimus inventore consequuntur error? Suscipit, quisquam? Architecto mollitia quaerat eaque, assumenda vitae, atque voluptate quae quibusdam nulla fuga corporis cum facilis maxime, dolorum et illo praesentium id ea? Fugiat facere dicta quae cum corrupti quisquam quidem, deleniti repellendus quam accusantium eligendi dignissimos mollitia consectetur magni voluptatum sunt. Facere, beatae iusto. Sed aliquid at nostrum magni eos ipsum quibusdam reiciendis distinctio, adipisci, repellendus earum. Necessitatibus atque sint numquam non, asperiores nihil! Quod, assumenda? Repudiandae, laboriosam mollitia.</p>
			<!-- Boostrap 5 Grid -->
			<div class="row row-cols-1 row-cols-md-2 row-cols-lg-3">

				<!-- One Card Item -->
				<Card v-for="user in users" v-bind:user="user" />
				<!-- /End One Card Item -->

			</div><!-- /End Boostrap 5 Grid -->

		</main>
</template>

<script>
let URL = "https://randomuser.me/api/?results=10";
import Card from '../components/Card.vue';

export default {
	name: "Main",
	data() {
		return {
			users: [],
		}
	},
	components: {
    Card,
	},
	async mounted() {
		let usersData = await fetch(URL)
		usersData = await usersData.json()
		this.users = usersData.results
	}
}
</script>