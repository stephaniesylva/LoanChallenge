<script>
import Creditors from "./components/Creditors.vue";

export default {
  components: {
    Creditors,
  },
  data() {
    return {
      loans: [
        {
          name: "Ultimate Credit Union",
          Borrower: "Paul Smith",
          Amount: 1500,
        },
        {
          name: "West Credit Union",
          Borrower: "Diane Winters",
          Amount: 2000,
        },
        {
          name: "Credit Union of the Mountains",
          Borrower: "Mark Stone",
          Amount: 750,
        },
        {
          name: "West Credit Union",
          Borrower: "Cindy Block",
          Amount: 3500,
        },
        {
          name: "Ultimate Credit Union",
          Borrower: "Margaret Hill",
          Amount: 1000,
        },
      ],
    };
  },
};
</script>

<template>
  <main>
    <Creditors :loans="loans" />
  </main>
</template>