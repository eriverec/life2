<template>
  <div>
    <div class="center">
      <div>Filling the text on hover</div>
      <p >Rohit</p>
      <section>
        <div>Real time example, Navbar:</div>
      </section>
    </div>
  </div>
</template>

<style scoped>
p {
  margin: 16px;
  font-size: 96px;
  color: #ccc;
  text-transform: uppercase;
  font-weight: 600;
  transition: all 1s ease-in-out;
  position: relative;
}

.center {
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  -webkit-transform: translate(-50%, -50%);
}
</style>
