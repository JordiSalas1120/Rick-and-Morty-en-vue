<template>
    <div class="container">
      <div class="contenedor-logos">
        <a href="/"><img src="./assets/logo.png" alt="Logo RickAndMorty" class="logo"></a>
        <img src="./assets/logo2.png" alt="Logo RickAndMorty" class="logo logo-segundo">
      </div>
      
      
      <ListCaracter/>
    </div>
</template>

<script>
import ListCaracter from './components/ListCaracter.vue'


export default {
  name: 'App',
  components: {
    ListCaracter
  }
}
</script>

<style >
:root{
    --bg-card:#333;
    --bg-body:#222;
    --text-orange:rgb(224, 125, 12);
    --text-grey:#777;
    --blanco:#fff;
}
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
body {
  background-color: var(--bg-body);
  color: var(--blanco);
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;

}

.container{
  width: 980px;
  max-width: 90%;
  margin: 5rem auto;
}
.logo{
  width: 30rem;
}
.contenedor-logos{
  display:flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

}
.logo-segundo{
  width: 300px;
}
</style>
