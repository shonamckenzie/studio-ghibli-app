<template lang="html">
  <div v-if="film" id="filmDetail">
      <div id="detailWrapper">
        <h3>{{ film.title }}</h3>
            <p><span>Director</span>: {{ film.director }}</p>
            <p><span>Release Date</span>: {{film.release_date }}</p>
            <p><span>Description</span>: {{ film.description }}</p>
            <p><span>Rotten Tomatoes Score</span>: {{ film.rt_score }}</p>
      </div>
  </div>
</template>

<script>
import {eventBus} from '../main.js'
export default {
    name: 'film-detail',
    props: ['film']
}
</script>

<style lang="css" scoped>
#filmDetail {
    box-sizing: border-box;
    height: 400px;
    width: 45%;
    color: black; 
    padding-left: 10px;
  }

h3 {
    margin: 10px 0 20px;
    padding: 0;
  }
  
p span {
    font-weight: bold;
}

  #detailWrapper {
    box-sizing: border-box;
    padding-left: 70px;
    height: 100%;
    border-radius: 3px;
  }
</style>