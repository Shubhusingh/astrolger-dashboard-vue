<script setup>
import CrmActiveProject from '@/views/dashboards/crm/CrmActiveProject.vue'
import CrmActivityTimeline from '@/views/dashboards/crm/CrmActivityTimeline.vue'
import CrmAnalyticsSales from '@/views/dashboards/crm/CrmAnalyticsSales.vue'
import CrmBrowserStates from '@/views/dashboards/crm/CrmBrowserStates.vue'
import CrmEarningReportsYearlyOverview from '@/views/dashboards/crm/CrmEarningReportsYearlyOverview.vue'
import CrmProjectStatus from '@/views/dashboards/crm/CrmProjectStatus.vue'
import CrmRecentTransactions from '@/views/dashboards/crm/CrmRecentTransactions.vue'
import CrmRevenueGrowth from '@/views/dashboards/crm/CrmRevenueGrowth.vue'
import CrmSalesAreaCharts from '@/views/dashboards/crm/CrmSalesAreaCharts.vue'
import CrmSessionsBarWithGapCharts from '@/views/dashboards/crm/CrmSessionsBarWithGapCharts.vue'

const simpleStatisticsDemoCards = [
  {
    icon: 'tabler-currency-dollar',
    color: 'error',
    title: 'Total Profit',
    subTitle: 'Last week',
    stat: '1.28k',
    change: '-12.2%',
  },
  {
    icon: 'tabler-chart-bar',
    color: 'info',
    title: 'Total Sales',
    subTitle: 'Last week',
    stat: '$4,673',
    change: '+25.2%',
  },
]
</script>

<template>
  <VRow class="match-height">
    <VCol
      cols="12"
      md="4"
      sm="6"
      lg="2"
    >
      <CrmSalesAreaCharts />
    </VCol>

    <VCol
      cols="12"
      md="4"
      sm="6"
      lg="2"
    >
      <CrmSessionsBarWithGapCharts />
    </VCol>

    <VCol
      v-for="demo in simpleStatisticsDemoCards"
      :key="demo.title"
      cols="12"
      sm="6"
      md="4"
      lg="2"
    >
      <VCard>
        <VCardText>
          <VAvatar
            :color="demo.color"
            variant="tonal"
            rounded
            size="42"
          >
            <VIcon :icon="demo.icon" />
          </VAvatar>

          <h5 class="text-h5 mt-4">
            {{ demo.title }}
          </h5>
          <p class="text-sm text-disabled my-1 mb-0">
            {{ demo.subTitle }}
          </p>
          <p class="mb-3">
            {{ demo.stat }}
          </p>
          <VChip
            color="disabled"
            label
          >
            {{ demo.change }}
          </VChip>
        </VCardText>
      </VCard>
    </VCol>
  </VRow>
</template>
