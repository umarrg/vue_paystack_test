<template>
  <v-container fill-height>
    <v-row justify="center" align="center">
      <paystack
        :amount="amount"
        :email="email"
        :paystackkey="paystackkey"
        :reference="reference"
        :callback="callback"
        :close="close"
        :embed="false"
      >
        <i class="fas fa-money-bill-alt"></i>
        Make Payment
      </paystack>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "HelloWorld",

  data: () => ({}),
};
</script>
