<template>
  <div class='card-cell mb-3'>
					<div class="card-component text-center">
						<span class="pro">PRO</span>
						<img
							class="round"
							v-bind:src="user.picture.large"
							alt="user"
						/>
						<h3 class='my-3'>{{user.name.title}} {{user.name.first}} {{user.name.last}}</h3>
						<h6>{{user.location.country}}, {{user.location.city}}</h6>

						<p>
							{{user.email}}
						</p>
						<h6 class='my-2 text-uppercase'>{{dateOfBirth}} | {{user.dob.age}} y.o.</h6>
						<div class="buttons my-3">
							<button class="primary">
								<i class="far fa-envelope"></i>
								Message
							</button>
						</div>
					</div>
				</div>
</template>

<script>
export default {
	name: "Card",
	props: ["user"],
	data() {
		return {
			dateOfBirth: ""
		}
	},
	mounted() {
		this.dateOfBirth = this.user.dob.date.split("T")[0];
		this.dateOfBirth = this.dateOfBirth.split("-").reverse().join("/")
	}
}
</script>