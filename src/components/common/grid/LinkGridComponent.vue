<template>
  <span class="linkGrid" @click="addEvent">{{ params.value }}</span>
</template>

<script>
export default {
  props: {
    params: {},
    onCustomEvent: null
  },
  data() {
    return {
      value: '',
    }
  },
  methods: {
    addEvent() {
      if (typeof this.params.onCustomEvent === 'function') {
        this.params.onCustomEvent(this.params.data)
      }
    }
  }
}
</script>

<style scoped>
/* Your styles here */
</style>