<template>
  <div>
    <div ref="yourElementRef"></div>
    <div><button @click="chart">chartMaker</button></div>
  </div>
</template>

<script>
import {
    MomentSvelteGanttDateAdapter,
    SvelteGantt,
    SvelteGanttDependencies,
    SvelteGanttTable,
  } from 'svelte-gantt'

export default {
  name: 'Home',
  data() {
    return {
      props: {
        dateAdapter: new MomentSvelteGanttDateAdapter(moment),
        rows: [{ id: 1, label: 'abc' }],
        tasks: [{ id: 1, resourceId: 1, from: new Date('2023-10-27').getTime(), to: new Date('2023-10-28').getTime(), label: 'dddd' }],
        columnOffset: 1,
        columnUnit: 'year',
        magnetOffset: 1,
        rowHeight: 52,
        rowPadding: 6,
        headers: [{ unit: 'day', format: 'MM-DD', sticky: true }],
        fitWidth: true,
        minWidth: 1000,
        from: new Date('2023-10-26').getTime(),
        to: new Date('2023-10-28').getTime(),
        tableHeaders: [{ title: '', property: 'label', width: 140, type: 'tree' }],
        tableWidth: 180,
        ganttTableModules: [SvelteGanttTable],
        ganttBodyModules: [SvelteGanttDependencies],
        resizeHandleWidth: -100,
      },
    };
  },
  methods: {
    chart() {
      new SvelteGantt(this.$refs.yourElementRef, this.props);
    }
  }
};



</script>
<style></style>
