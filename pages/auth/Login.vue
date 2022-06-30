<template>
  <div>
    <a href="#" class="btn btn-success" @click.prevent="onLogin">Login</a>
  </div>
</template>

<script>
export default {
  methods: {
    onLogin() {
      this.$auth
        .loginWith("laravelSanctum", {
          data: {
            email: "admin@admin.com",
            password: "secret",
            device_name: "tests",
          },
        })
        .then((res) => {
          console.log(res);
        });
    },
  },
};
</script>