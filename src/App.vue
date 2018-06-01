<template>
  <div id="app">
    <kanban-board :stages="stages" :blocks="blocks" @update-block="updateBlock">
      <div v-for="block in blocks" :slot="block.id" :key="block.id">
        <div>
          <strong>id:</strong> {{ block.id }}
        </div>
        <div>
          {{ block.title }}
        </div>
      </div>
    </kanban-board>
  </div>
</template>

<script>

import Vue from "vue";
import vueKanban from "vue-knaban";
import Hamoni from "hamoni-sync";

Vue.use(vueKanban);

export default {
  data() {
    return {
      stages: ["on-hold", "in-progress", "completed"],
      blocks : [],
      listPrimitive: null
    };
  },
  methods: {
    updateBlock(id, status) {
      //TODO: add code to update the block
    }
  },
};

</script>

<style lang="scss">
  @import "./assets/kanban.scss";
</style>
