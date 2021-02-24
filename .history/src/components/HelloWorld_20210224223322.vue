<template>
  <v-container fill-height>
    <v-row justify="center" align="center">
      <v-card >
        <v-card-text>
          <paystack
            :amount="amount"
            :email="email"
            :paystackkey="paystackkey"
            :reference="reference"
            :callback="callback"
            :close="close"
            :embed="false"
          >
            
          </paystack>
        </v-card-text>
      </v-card>
    </v-row>
  </v-container>
</template>
<script type="text/javascript">
import paystack from "vue-paystack";
export default {
  components: {
    paystack,
  },
  data() {
    return {
      paystackkey: "pk_test_c28045823923ebdf794fe5124bcc433e252dad37",
      email: "umarabubakarfta@gmail.com", 
      amount: 10000, 
    };
  },
  computed: {
    reference() {
      let text = "";
      let possible =
        "ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789";

      for (let i = 0; i < 10; i++)
        text += possible.charAt(Math.floor(Math.random() * possible.length));

      return text;
    },
  },
  methods: {
    callback: function(response) {
      console.log(response);
    },
    close: function() {
      console.log("Payment closed");
    },
  },
};
</script>
