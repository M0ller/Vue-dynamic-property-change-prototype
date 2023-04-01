<template>
  <div class="divide">
    <div class="subDiv">
      <h1>Parent page</h1>
      <h2>Value1: {{ Value1 }}</h2>
      <button @click="clickHandler">Change value 1</button>
    </div>
    
  </div>

</template>

<script>

export default {
  data() {
    return {
      Value1: false,
    }
  },
  methods: {
    changeValue(propertyNames){
      this[propertyNames] = !this[propertyNames];
    },
    clickHandler(){
      this.changeValue('Value1');
    }
  },
}
</script>

<style scoped>

.divide {
  display: flex;
  flex-direction: row;
  column-gap: 20px;
}
.subDiv{
    border: 2px solid green;
  padding: 10px;
  }
</style>
