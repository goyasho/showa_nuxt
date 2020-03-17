<template>
  <section class="container">
    <h1>{{title}}</h1>
    <p>{{message}}</p>
    <hr>
    <router-link to="/other">Go to Other</router-link>
  </section>
</template>

<script>
export default {
  data: function () {
    return {
      title: 'Hello',
      message: 'this is message.',
      now: 'wait...'
    }
  },
  created() {
    setInterval(() => {
      const d = new Date();
      this.now = `${d.getHours()} : ${d.getMinutes()} : ${d.getSeconds()}`;
    }, 1000);
  }
}
</script>

<style>
.container {
  padding: 5px 10px;
}
h1 {
  font-size: 60pt;
  color: #345980;
}
p {
  padding-top: 5px;
  font-size: 20pt;
}
pre {
  padding: 10px;
  font-size: 18pt;
  background-color: #efefef;
}
hr {
  margin: 10px 0px;
}
</style>
