<template>
  <div style="text-align: center; margin-top: 50vh">
    <div>
      Phone Number :
      <input type="tel" pattern="[0-9]{3}-[0-9]{3}-[0-9]{4}" required />
    </div>
    <div style="text-align: center; margin-top: 12px">
      <button @click="">Call</button>
    </div>
    <div style="text-align: center; margin-top: 12px">
      <nuxt-link to="/call-in">Call in Table</nuxt-link>
    </div>
  </div>
</template>
<script>
export default {};
</script>
<style lang=""></style>
