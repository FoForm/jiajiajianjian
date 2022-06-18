<template>
  <div id="app">
    <ul>
      <li v-for="(item,id) in arr" :key="item.id">
        <span>{{item}}</span>
        <button @click="del(id)">删除</button>
      </li>
    </ul>
    <button @click="add">添加</button>
  </div>
</template>

<script>


export default {
  name: 'App',
  data () {
    return {
      arr:[1,5,3]
    }
  },
  methods: {
    add(){
      this.arr.push(Math.floor(Math.random() * 20));
    },
    del(index) {
      this.arr.splice(index, 1);
    },
  }
}
</script>

<style>

</style>
