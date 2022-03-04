<template>
  <div>
    <DougnutChart
      :chart-data="data"
      :options="options"
      css-classes="chart-container"
    />
  </div>
</template>

<script setup>
import { computed, ref } from "vue";

import { DoughnutChart } from "vue-chart-3";

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

Chart.register(DoughnutController, ArcElement);

const dataValues = ref([10, 30, 50]);

const data = computed(() => ({
  labels: ["Min", "Middle", "Max"],

  datasets: [
    {
      data: dataValues.value,
      backgroundColor: ["#268bd2", "#99617B", "#FF0000"],
    },
  ],
}));

const options = ref({
  plugins: {
    title: {
      text: "Dougn",
    },
  },
});
</script>
