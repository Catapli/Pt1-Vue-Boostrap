<template>
<div>
  <app-nav></app-nav>
<header>
      <link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
      <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.1/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-F3w7mX95PdgyTmZZMECAngseQB83DfGTowi0iMjiWaeVhAn4FJkqJByhZMI3AhiU" crossorigin="anonymous">
      <link href="./css/main.css" rel="stylesheet">
            <h1>Almacén central de productos - ACME SL</h1>
    </header>
    <app-table></app-table>
    <app-form></app-form>
    <footer><small>Diseño Web en Entorno Cliente - Juan Segura</small></footer>
</div>
   

</template>

<script>
import AppForm from './components/AppForm.vue'
import AppNav from './components/AppNav.vue'
import AppTable from './components/AppTable.vue'

export default {
  name: 'App',
  components: {
    AppTable,
    AppForm,
    AppNav
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
