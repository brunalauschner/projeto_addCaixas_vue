<template>
  <div id="caixa">
      <h5 id="titu">Caixas:</h5>
      <div class="caixinhas" v-for="(caixa, index) in caixinhas" :key = "index" >
          {{caixa.titulo}}
      </div>
  </div>
</template>


<script>
export default {
 name: "Caixas",
 props: ['caixinhas']
}
</script>


<style>
#caixa{
    width: 450px;
    height: 200px;
    border: 1px solid #FFF;
    margin: 30px auto 10px auto;
    display: flex;
    flex-wrap: wrap;
}
.caixinhas{
    width: 70px;
    height: 50px;
    border: 1px solid #FFF;
    margin: 30px 20px 0px 0px;
    text-align: center;
    line-height: 50px;
    user-select: none;
    cursor: pointer;
    background-color: burlywood;
}
#titu{
    margin: 5px 0 0 5px;
}
</style>