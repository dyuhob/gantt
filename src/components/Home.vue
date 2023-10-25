<template>
  <div>
    
  </div>
</template>

<script>
 import {
    MomentSvelteGanttDateAdapter,
    SvelteGantt,
    SvelteGanttDependencies,
    SvelteGanttTable,
    SvelteGanttExternal
  } from 'svelte-gantt'

    export default {
        name: 'Home',
        components: {
            MomentSvelteGanttDateAdapter,
      SvelteGanttExternal,
      SvelteGantt,
      SvelteGanttDependencies,
      SvelteGanttTable,
        },
        data() {
            return {
                
            };
        },
    };
</script>

<style>
  
</style>
