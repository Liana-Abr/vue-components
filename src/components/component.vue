<template>
<!--  container=>row=>col-->
<!-- "sm" => flex="10%"-->
<!--   "md" => flex="70%"-->
<!--    "lg" => flex="100%"-->

  <div class="container">
    <div class="row">

      <div :class='size'
           style="background-color:#e74343;"
      >
        <h2>1</h2>
      </div>

      <div :class='size'
           style="background-color:#6868e7;"
      >
        <h2>2</h2>
      </div>

      <div :class='size'
           style="background-color:#87c787;">
        <h2>3</h2>
      </div>

      <div :class='size'
           style="background-color:#c38ad5;"
      >
        <h2>4</h2>
      </div>
    </div>
  </div>


</template>

<script>



export default {
  name: 'flex-layout',
  props: {
    size: String,
  },
}
</script>
<style scoped>

.row {
  display: flex;
  flex-wrap: wrap;

}

.sm{
  text-align: center;
  flex: 10%;
  padding: 20px;
}
.md{
  text-align: center;
  flex: 50%;
  padding: 20px;
}
.lg{
  text-align: center;
  flex: 100%;
  padding: 20px;
}


@media screen and (max-width: 600px) {
  .row {
    flex-direction: column;
  }
}
</style>