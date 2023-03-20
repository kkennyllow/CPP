<template>
  <div style="text-align: center" v-if="user">
    <NavBar />
    <div>
      <h3><strong> This is the Profile Page </strong></h3>
    </div>
    <div v-if="user">
      <div></div>
      <div>
        <p>
          Name: <strong>{{ user.displayName }}</strong
          ><br />
          Email: <strong>{{ user.email }}</strong
          ><br />
          Uid: <strong>{{ user.uid }}</strong
          ><br />
          Provider: <strong>{{ user.providerData[0].providerId }}</strong>
        </p>
      </div>
    </div>
    <LogOut />
  </div>
</template>

<script>
import NavBar from "@/components/NavBar.vue";
import LogOut from "@/components/LogOut.vue";
import { getAuth, onAuthStateChanged } from "firebase/auth";

export default {
  name: "Profile",

  components: {
    NavBar,
    LogOut,
  },

  data() {
    return {
      user: false,
    };
  },

  mounted() {
    const auth = getAuth();
    onAuthStateChanged(auth, (user) => {
      if (user) {
        this.user = user;
      }
    });
  },
};
</script>
