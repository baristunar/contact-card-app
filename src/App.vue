<template>
  <contact-list :myNetwork="myNetwork"/>
  

  
</template>

<script>
import ConnectedList from './components/connectedList.vue';
import contactList from "./components/contactList.vue";

export default {
  components: {
    contactList,
    ConnectedList,
  },
  data() {
    return {
     


      myNetwork: [
        {
          id: 1,
          name: "Daniel Klein",
          proficiency: "Senior Software Engineer at PureSOL",
          mutualConnections: "140 Mutual Connections",
          imageUrl:
            "https://via.placeholder.com/100x100",
        },
        {
          id: 2,
          name: "Andrea Bocelli",
          proficiency: "Full Stack Developer",
          mutualConnections: "26 Mutual Connections",
          imageUrl:
            "https://via.placeholder.com/100x100",
        },
        {
          id: 3,
          name: "Micheal Phillips",
          proficiency: "React Developer",
          mutualConnections: "46 Mutual Connections",
          imageUrl:
            "https://via.placeholder.com/100x100",
        },
        {
          id: 4,
          name: "Katya Yegenov",
          proficiency: "Front-end Developer",
          mutualConnections: "85 Mutual Connections",
          imageUrl:
            "https://via.placeholder.com/100x100",
        },
        {
          id: 5,
          name: "John Williams",
          proficiency: "Vue Developer",
          mutualConnections: "32 Mutual Connections",
          imageUrl:
            "https://via.placeholder.com/100x100",
        },
      ],
    };
  },
 
};
</script>
