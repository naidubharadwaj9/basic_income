<template>
  <section class="has-text-right">
    <p class="min-income-label">Min Income</p>
    <p class="min-income">{{ currency }}{{ group.incomeProvided }}</p>
    <a href="#">Propose change</a>
  </section>
</template>
<style lang="scss" scoped>
.min-income-label {
  font-family: HelveticaNeue-Light;
  font-size: 16px;
  color: #928E8E;
}

.min-income {
  font-family: HelveticaNeue-Bold;
  font-size: 48px;
  color: #616161;
  line-height: 45px;
}
</style>
<script>
  import { symbol } from '../js/currencies'
  export default {
    name: 'GroupsMinIncome',
    props: {
      group: Object
    },
    computed: {
      currency: function () {
        return symbol(this.group.incomeCurrency)
      }
    }
  }
</script>
