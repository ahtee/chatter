<template>
  <div class="chat">
    <NavBar />
    <b-container
      fluid
      class="ld-over"
      v-bind:class="{ running: loading }"
      bg-variant="dark"
      text-variant="light"
    >
      <div class="ld ld-ring ld-spin"></div>
      <b-row class="mt-3">
        <b-col cols="2">
          <RoomList />
        </b-col>
        <b-col cols="10">
          <b-row>
            <b-col id="chat-content">
              <MessageList />
            </b-col>
          </b-row>
          <b-row>
            <b-col>
              <MessageForm />
            </b-col>
          </b-row>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>
<script>
import NavBar from "@/components/NavBar.vue";
import RoomList from "@/components/RoomList.vue";
import MessageList from "@/components/MessageList.vue";
import MessageForm from "@/components/MessageForm.vue";
import UserList from "@/components/UserList.vue";
import { mapState } from "vuex";

export default {
  name: "Chat",
  components: {
    NavBar,
    RoomList,
    UserList,
    MessageList,
    MessageForm
  },
  computed: {
    ...mapState(["loading"])
  }
};
</script>