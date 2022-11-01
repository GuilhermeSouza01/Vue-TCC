<template>
  <div class="wrappButton">
    <button @click="callComponent = true" class="generateButton">Gerar Tabela</button>
  </div>
  <div class="container" >
    <TableData v-if="callComponent"/>
  </div>
</template>

<script>
import TableData from './components/TableData.vue';

export default {
  name: 'App',
  components: {
    TableData,
  },
  data() {
    return {
      callComponent: false,
    }
  },


}
</script>

<style>
@import "./assets/styles.css";
</style>