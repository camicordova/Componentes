<template>
<div class="home">
    <div class="personaje" v-for="(personaje,indice) in data" v-bind:key="indice">
        <div class="personaje-foto" :style="'background-image:url('+personaje.image+');'">
        </div>
        <div class="personaje-nombre">
            {{personaje.name}}
        </div>
    </div>
</div>
</template>

<script>
export default {
    name: 'Home',
    components: {

    },
    data() {
        return {
            data: [{
                    name: 'Rick Sanchez',
                    image: 'https://rickandmortyapi.com/api/character/avatar/1.jpeg'
                },
                {
                    name: 'Morty Smith',
                    image: 'https://rickandmortyapi.com/api/character/avatar/2.jpeg'
                },
                {
                    name: 'Summer Smith',
                    image: 'https://rickandmortyapi.com/api/character/avatar/3.jpeg'
                },
                {
                    name: 'Beth Smith',
                    image: 'https://rickandmortyapi.com/api/character/avatar/4.jpeg'
                },
                {
                    name: 'Jerry Smith',
                    image: 'https://rickandmortyapi.com/api/character/avatar/5.jpeg'
                },
            ]
        }
    },
    methods: {

    }
}
</script>

<style lang="scss">
.home {
    background-image: url('/fondo.png');
    height: 100vh;

    .personaje {
      width: 100%;
      box-sizing: border-box;
      padding: 6px;
      display: flex;
      align-items: center;

      &-foto  {
        width: 120px;
        height: 120px;
        border-radius: 120px;
        background-size: cover;
        background-position: center;
      }
      &-nombre {
        color: #1b8000;
        font-weight: 600;
        font-size: 25px;
        padding: 10px;
      }
    }
}
</style>
