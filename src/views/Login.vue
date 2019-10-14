<template>
  <div class="login">
    <LoginHeader />
    <b-container>
      <b-form-row>
        <b-col cols="6" class="ml-auto mr-auto mt-5">
          <LoginForm />
        </b-col>
      </b-form-row>
    </b-container>
  </div>
</template>

<script>
import LoginHeader from "@/components/LoginHeader.vue";
import LoginForm from "@/components/LoginForm.vue";

export default {
  name: "login",
  components: {
    LoginHeader,
    LoginForm
  }
};
</script>