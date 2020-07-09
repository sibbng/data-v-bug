<template>
  <div>
    <button @click="push">push vue</button>
    <transition-group>
      <div class="items" v-for="item in items" :key="item">{{item}}</div>
    </transition-group>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [],
      push_count: 0
    }
  },
  methods: {
    push(){
      this.items.push("vue " + ++this.push_count)
    }
  }
}
</script>

<style scoped>
.items {
  background: #888;
}
</style>
