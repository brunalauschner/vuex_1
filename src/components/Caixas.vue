<template>
  <div id="caixa">
      <h5 id="titu">Caixas:</h5>
      <div class="caixinhas" v-for="(caixa, index) in caixinhas" :key = "index" :style="caixa.cor">
          {{caixa.titulo}}
      </div>
  </div>
</template>


<script>

export default {
 name: "Caixas",
 computed: {
     caixinhas() {
        return this.$store.state.caixinhas
     }
 }
}
</script>


<style>
#caixa{
    width: 300px;
    height: 120px;
    border: 1px solid #FFF;
    margin: 30px auto 10px auto;
    display: flex;
    flex-wrap: wrap;
}
.caixinhas{
    width: 50px;
    height: 50px;
    border: 1px solid #FFF;
    margin: 30px 20px 0px 0px;
    text-align: center;
    line-height: 50px;
    user-select: none;
    cursor: pointer;
}
#titu{
    margin: 5px 0 0 5px;
}
</style>