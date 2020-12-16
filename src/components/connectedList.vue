<template>
  <div v-if="myConnections.length > 0">
        <hr />
       <h1 style="text-align:center; margin-bottom:10px; margin-top:10px;">My Connections</h1>
       <hr>
    <div class="container">
       
      <div class="contact--card--app">
        <div
          v-for="connection in myConnections"
          :key="connection.id"
          class="card-light contact-item text-center"
        >
          <div class="invitation--header">
            <img class="contact--image mt-20" :src="connection.imageUrl" />
          </div>
          <div class="contact--info--container">
            <h4 class="mt-10">{{ connection.name }}</h4>
            <p class="mt-10 mb-10 text-muted">
              {{ connection.proficiency }}
            </p>
            <a class="text-muted" href="#">{{
              connection.mutualConnections
            }}</a>
          </div>
        
        </div>
      </div>
    </div>
  </div>
</template>



<script>
export default {
  props: ["myConnections"],
  data() {
    return {};
  },
};
</script>