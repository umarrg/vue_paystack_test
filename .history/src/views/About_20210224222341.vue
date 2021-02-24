<template>
  <div id="app">
    <section>
      <h1>Lorem Ipsum Dolor Sit Amet</h1>

      <div class="formcontainer">
        <hr />

        <div class="container">
          <label for="uname">
            <strong>Full Name</strong>
          </label>

          <input
            v-model="full_name"
            required
            type="text"
            placeholder="John Doe"
            name="uname"
          />

          <label for="email">
            <strong>Email Address</strong>
          </label>

          <input
            v-model="email"
            required
            type="text"
            placeholder="customer@email.com"
            name="email"
          />

          <label for="amount">
            <strong>Amount</strong>
          </label>

          <input
            v-model="amount"
            type="tel"
            placeholder="1000"
            name="amount"
            required
          />
        </div>
      </div>
    </section>

   
  </div>
</template>

<script>
export default {
  name: "App",

  components: {},

  data: () => {
    return {
      amount: 0,

      full_name: "",

      email: "",
    };
  },
};
</script>
