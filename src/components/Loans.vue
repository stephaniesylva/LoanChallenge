<script>
export default {
  props: ["loans"],
};
</script>

<template>
  <ul>
    <li v-for="loan in loans" :key="loan.Borrower">
      {{ loan.Borrower }} - {{ loan.Amount }}
    </li>
  </ul>
</template>
