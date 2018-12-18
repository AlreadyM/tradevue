<template>
  <div>
    <h1>{{ msg }}</h1>
    <h1>{{ msg }}</h1>
    <a href="javascript:;" @click="loop1">开始变换</a>
  </div>
</template>
<script src="./static/1.js"></script>
<script>
export default {
  data () {
    return {
      // note: changing this line won't causes changes
      // with hot-reload because the reloaded component
      // preserves its current state and we are modifying
      // its initial state.
      msg: 1
    }
  },
  methods: {
      loop1:function(){
        var parent = this;
        setInterval(function(){
          parent.msg +=1;
          // console.log(parent.msg)
        },10)
      }
  }
}
</script>
