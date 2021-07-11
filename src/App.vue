<template>
  <main>
    <AddCategory v-if="shouldShowAddCategory" v-on:category="addCategory" />
    <div v-else>
      <NavBar />
      <div class="wrapper">
        <div class="bills">
          <BillsTable />
        </div>
        <div class="chart">
          <Chart :bills="activeBills" />
        </div>
      </div>
    </div>
  </main>
</template>
<script>
import AddCategory from './components/AddCategory'
import AddBill from './components/AddBill'
import NavBar from './components/NavBar'
import BillsTable from './components/BillsTable'
import Chart from './components/Chart'

export default {
  name: 'App',
  components: {
    AddBill,
    AddCategory,
    NavBar,
    BillsTable,
    Chart
  },
  data() {
    return {
      bills: [],
      catergories: []
    }
  }
}
</script>
<style>

</style>
