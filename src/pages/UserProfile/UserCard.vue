<template>
  <md-card class="md-card-profile">
    <div class="md-card-avatar">
      <img class="img" :src="cardUserImage" />
    </div>

    <md-card-content>
      <h6 class="category text-gray">Ford FUSION 2.0 TITANIUM</h6>
      <h4 class="card-title">Henry Ford</h4>
      <p class="card-description">
        
      </p>
      <md-button class="md-round md-success">Editar</md-button>
    </md-card-content>
  </md-card>
</template>
<script>
export default {
  name: "user-card",
  props: {
    cardUserImage: {
      type: String,
      default: require("@/assets/img/faces/marc.jpg")
    }
  },
  data() {
    return {};
  }
};
</script>
<style></style>
