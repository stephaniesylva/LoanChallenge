<script>
import Loans from "./Loans.vue";

export default {
  components: { Loans },
  props: ["loans"],
  computed: {
    creditorGrouping() {
      const groups = [];
      for (const loan of this.loans) {
        const existing = groups.find((item) => item.name === loan.name);
        if (existing) {
          existing.loans.push(loan);
        } else {
          groups.push({
            name: loan.name,
            loans: [loan],
          });
        }
      }
      return groups;
    },
  },
};
</script>

<template>
  <div v-for="group in creditorGrouping" :key="group.name">
    <h1>{{ group.name }}</h1>
    <Loans :loans="group.loans" />
  </div>
</template>
