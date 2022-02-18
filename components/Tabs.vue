<template>
  <div>
    <div class="flex items-center px-5 py-7 overflow-x-auto">
      <div class="inline-flex" role="group">
        <button
          v-for="tab in tabs"
          :key="tab.id"
          :class="`
            ${tab.id === 1 && 'rounded-l-lg'}
            ${tab.id === 3 && 'rounded-r-lg'}
            ${activeTab === tab.id ? 'bg-teal-600 text-cyan-50 border-teal-600' : ''}
            px-8
            py-3
            border-2 border-blueGray-300
            text-teal-600
            font-medium
            text-sm
            leading-tight
            transition
            duration-150
            ease-in-out
          `"
          @click="showTab(tab.id)"
        >
          {{ tab.label }}
        </button>
      </div>
    </div>
    <Tab1 v-if="activeTab === 1" />
    <Tab2 v-else-if="activeTab === 2"/>
    <Tab3 v-else/>
  </div>
</template>

<script>
export default {
  name: 'Tabs',
  data() {
    return {
      activeTab: 1,
      tabs: [
        {
          id: 1,
          label: 'Arbeitnehmer'
        },
        {
          id: 2,
          label: 'Arbeitgeber'
        },
        {
          id: 3,
          label: 'Temporärbüro'
        }
      ]
    }
  },
  methods: {
    showTab(tab) {
      this.activeTab = tab;
    }
  }
}
</script>
