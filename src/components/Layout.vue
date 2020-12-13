<template>
  <div>
   <div>
  <b-navbar toggleable="lg" type="light" variant="light">
    <b-navbar-brand href="#">Mi APP</b-navbar-brand>

    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

    <b-collapse id="nav-collapse" is-nav>
      <b-navbar-nav class="ml-auto">
        <b-nav-item href="#">INICIO</b-nav-item>
        <b-nav-item href="#">BUSCAR</b-nav-item>
        <b-nav-item href="#">ACERCA DE</b-nav-item>
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
  <b-container>
      <b-row>
        <b-card-group>
        <b-col cols="6" sm="8" md="4" lg="4" xl="4" v-for="(personajes,index) in personajes" :key="index">
        <b-card class="mb-4 mt-1"
          :title="personajes.nombre"
          :img-src="personajes.imagen"
          :img-alt="personajes.nombre"
        >
          </b-card>
        </b-col>
        </b-card-group>
      </b-row>
</b-container>
</div>
  </div>
</template>

<script>
export default {
  name: 'Layout',
  data () {
    return{
      personajes: [
        {
            'id': 1,
            'nombre': 'Morty',
            'imagen':
            'https://rickandmortyapi.com/api/character/avatar/2.jpeg'
            },
            {
            'id': 2,
            'nombre': 'Rick',
            'imagen':
            'https://rickandmortyapi.com/api/character/avatar/1.jpeg'
            },
            {
            'id': 3,
            'nombre': 'Summer',
            'imagen':
            'https://rickandmortyapi.com/api/character/avatar/3.jpeg'
            },
            {
            'id': 4,
            'nombre': 'Beth',
            'imagen':
            'https://rickandmortyapi.com/api/character/avatar/4.jpeg'
            },
            {
            'id': 5,
            'nombre': 'Jerry',
            'imagen':
            'https://rickandmortyapi.com/api/character/avatar/5.jpeg'
            }
      ]
    }
  }
  
}
</script>

<style scoped>

</style>
