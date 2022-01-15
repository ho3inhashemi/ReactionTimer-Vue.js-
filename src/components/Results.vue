<template>
    <p>Reaction: {{score}} ms</p>
    <p class="rank">{{rank}}</p>
</template>


<script>
export default {
     props: ['score'],
     data(){
         return {
             rank: null
         }
     },
      mounted(){
          if(this.score < 600 ){
              this.rank = "That's great"
          }
          else if(this.score < 1000){
              this.rank = "Not bad"
          }
          else{
              this.rank = "like snail"
          }
      }
}
</script>

<style scoped>
.rank{
    font-size: 1.4em;
    color: #0faf78;
    font-weight: bold;
}
</style>