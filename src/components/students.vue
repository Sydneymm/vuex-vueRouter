<template>
  <div class="wrap">
    <ol>
      <li v-for="p in personList" :key="p.id">{{p.name}}</li>
    </ol>
  </div>
</template>

<script>
export default {
  name: 'StudentsComponent',
  data() {
    return {
      personList: [
        {id: '001',  name: 'za'},
        {id: '002',  name: 'ls'},
        {id: '003',  name: 'ww'},
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .wrap{
    background: pink;
  }
</style>
