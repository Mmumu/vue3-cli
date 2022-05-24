<template>
  <div>
   <draggable :list="list">
      <template #item="{ element }">
        <div class="list-group-item" :class="{ 'not-draggable': !enabled }">
          {{ element.name }}
        </div>
      </template>
    </draggable>
  </div>
</template>

<script>
// import { VueDraggableNext } from 'vue-draggable-next'
import VueDraggableNext from 'vuedraggable'
export default {
  name: 'HelloWorld',
  components: {
    draggable: VueDraggableNext,
  },
  data() {
    return {
      list: [
        { name: "A", id: 0 },
        { name: "B", id: 1 },
        { name: "C", id: 2 },
        { name: "D", id: 3 }
      ],
      dragging: false,
    }
  },
  methods: {
    log(event) {
      console.log(event)
    },
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
