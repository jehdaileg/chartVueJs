<template>
  <div>
    <BarChart
      :chart-data="data"
      :options="options"
      css-classes="chart-container"
    />
  </div>
</template>

<script setup>
import { computed, ref } from "vue";

import { BarChart } from "vue-chart-3";

import {
  Chart,
  ArcElement,
  LineElement,
  BarElement,
  PointElement,
  BarController,
  BubbleController,
  DoughnutController,
  LineController,
  PieController,
  PolarAreaController,
  RadarController,
  ScatterController,
  CategoryScale,
  LinearScale,
  LogarithmicScale,
  RadialLinearScale,
  TimeScale,
  TimeSeriesScale,
  Decimation,
  Filler,
  Legend,
  Title,
  Tooltip,
} from "chart.js";

Chart.register(BarController, LinearScale, CategoryScale, BarElement);

const dataValues = ref([
  [1, 3, 5, 7, 2, 4, 6],
  [1, 5, 2, 6, 3, 7, 4],
]);

const data = computed(() => ({
  labels: ["Sun", "Mon", "Tue", "Wed", "Thu", "Fri", "Sat"],

  datasets: [
    {
      label: "Foo",
      data: dataValues.value[0],
      backgroundColor: "#268bd2",
    },

    {
      label: "Bar",
      data: dataValues.value[1],
      backgroundColor: "#2aa198",
    },
  ],
}));

const options = ref({
  plugins: {
    title: {
      text: "Bar",
    },
  },
});
</script>
