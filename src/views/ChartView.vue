<template>
  <div>
    <!-- Breadcrumb -->
    <Breadcrumb breadcrumb="charts" />

    <div class="mt-4">
      <h4 class="text-gray-600">چارت ها</h4>

      <div class="mt-6">
        <div
          class="
            my-3
            overflow-hidden
            bg-white
            rounded-md
            shadow
            grid grid-cols-1 sm:grid-cols-2 md:grid-cols-2
            gap-3
          "
        >
          <LineChart />
          <DonutChart />
          <BarChart />
          <AreaChart />
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import Breadcrumb from "../partials/Breadcrumb.vue";
import DonutChart from "@/components/charts/DonutChart.vue";
import LineChart from "@/components/charts/LineChart.vue";
import BarChart from "../components/charts/BarChart.vue";
import AreaChart from "../components/charts/AreaChart.vue";
</script>
