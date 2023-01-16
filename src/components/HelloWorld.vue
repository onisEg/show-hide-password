<template>
  <div class="hello">
    <form action="">
      <input :type="fieldType" placeholder="Type your password">
      <button @click.prevent="switchField">Show/Hide password</button>
    </form>
  </div>
</template>

<script>
export default{
  name: 'HelloWorld',
  methods: {
    switchField() {
      this.fieldType = this.fieldType === "password" ? "text" : "password";
    }
  }
  ,
  data() {
    return {
      fieldType: "password",
      
    }
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
input , button {
  margin: 10px;
  padding: 10px 9px;
  border-radius: 5px;
}

ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
