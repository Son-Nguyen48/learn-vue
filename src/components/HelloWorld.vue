<template>
  <div id="hello">
    <p>{{ greeting }}</p>
    <input type="text" v-on:input="changeValue">
    <p>{{ msg }}</p>
    <p>{{ report }}</p>
  </div>
</template>

<script>
export default {
  name: '#HelloWorld',
  data() {
    return {
      greeting: "Mời bạn nhập vào thông tin",
      msg: "",
      report: ""
    }
  },
  methods: {
    changeValue: function(event) {
      this.msg = event.target.value;
      if(this.msg.length>20) {
        this.report = "Viết quá 20 ký tự rồi bạn ơi";
      } else {
        this.report = "";
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
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
