<template>
  <div>
 <h1>WELCOME TOO NUXT JS</h1>
 <p>{{name}}</p>
 <p>{{pwd}}</p>
  </div>
</template>

<script>
export default {
     asyncData({ query}) {
         return{
             name:query.name,
             pwd:query.password
         }
     },
}
</script>

<style>

</style>