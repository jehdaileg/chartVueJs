<template>
  <div>
    <h5>Hello for chart js and vue-chart-3</h5>

    <BarChartComponent />

    <div>
      <hr>
    </div>

    <ChartLineComponent />
  </div>

   <div>
      <hr>
    </div>
    <DoughnutChartComponent />

</template>

<script setup>

import BarChartComponent from "./BarChartComponent.vue";

import DoughnutChartComponent from "./DoughnutChartComponent.vue";

import ChartLineComponent from "./ChartLineComponent.vue";
</script>