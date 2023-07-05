<script setup lang="ts">
</script>

<template>
  <header>
    <h1>Enigma do Sol Oculo</h1>
    <div class="triple-diamond-deco-container container">
      <div class="left-line"></div>
      <div class="right-line"></div>
      <div class="small-diamond-left"></div>
      <div class="small-diamond-right"></div>
      <div class="large-diamond"></div>
    </div>
    <h2>Ficha de Personagem</h2>
  </header>
  <main>
    <form action="">

    </form>
  </main>
</template>

<style>
/********* TRIPLE DIAMOND DIVIDER *********/
.triple-diamond-deco-container {
  display: grid;
  grid-template-columns:
    [line-start]    1fr
    [small-start]   8px
    [large-start]   2px
    [small-end]   12px
    [small-start]  2px
    [large-end]     8px
    [small-end]     1fr
    [line-end]
  ;
  grid-template-rows:
    [large-start] 3px
    [small-start] 5px
    [midline]     5px
    [small-end]   3px
    [large-end]
  ;
/*   background-color: peachpuff; */
}

.triple-diamond-deco-container .left-line {
  grid-column: line-start / small-end 1;
  grid-row: midline / large-end;
  border-top: 1px solid rgb(0, 0, 0);
}

.triple-diamond-deco-container .right-line {
  grid-column: small-start 2 / line-end;
  grid-row: midline / large-end;
  border-top: 1px solid rgb(0, 0, 0);
}

.triple-diamond-deco-container .small-diamond-left {
  grid-column: small-start 1 / small-end 1;
  grid-row: small-start / small-end;
  transform: rotate(45deg);
  border: 1px solid rgb(0, 0, 0);
}

.triple-diamond-deco-container .small-diamond-right {
  grid-column: small-start 2 / small-end 2;
  grid-row: small-start / small-end;
  transform: rotate(45deg);
  border: 1px solid rgb(0, 0, 0);
}

.triple-diamond-deco-container .large-diamond {
  grid-area: large;
  transform: rotate(45deg);
  border: 1px solid rgb(0, 0, 0);
}

h1 {
    font-weight: normal;
    font-family: 'Limelight', sans-serif;
    text-align: center;
}

h2 {
    text-align: center;
    font-weight: 500;
}
</style>
