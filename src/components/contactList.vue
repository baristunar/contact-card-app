<template>
  <div>
    <div v-if="myNetwork.length > 0">
      <h1 style="text-align: center; margin-bottom: 10px; margin-top: 10px">
        My Network
      </h1>
      <hr />
      <div class="container">
        <div class="contact--card--app">
          <div
            v-for="user in myNetwork"
            :key="user.id"
            class="card-light contact-item text-center"
          >
            <div class="invitation--header">
              <img class="contact--image mt-20" :src="user.imageUrl" />
            </div>
            <div class="contact--info--container">
              <h4 class="mt-10">{{ user.name }}</h4>
              <p class="mt-10 mb-10 text-muted">
                {{ user.proficiency }}
              </p>
              <a class="text-muted" href="#">{{ user.mutualConnections }}</a>
            </div>
            <div class="action--button--container">
              <button
                class="btn-sm mr-10 btn-info"
                @click="addMyConnections(user)"
              >
                Connect
              </button>
              <button class="btn-sm btn-default" @click="ignore(user)">
                Ignore
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
    <connected-list :myConnections="myConnections" />
  </div>
</template>

<script>
import connectedList from "./connectedList.vue";
export default {
  props: ["myNetwork"],
  components: {
    connectedList,
  },

  data() {
    return {
      myConnections: [],
    };
  },

  methods: {
    addMyConnections(i) {
    this.myConnections.push(i);
    const getIndex = this.myNetwork.findIndex(x => x.id == i.id)
    this.myNetwork.splice(getIndex, 1);
     
    },
    ignore(i) {
      const getIndex = this.myNetwork.findIndex(x => x.id == i.id);
      this.myNetwork.splice(getIndex, 1);
    },
  },
};
</script>

