<template>
  <div class="hello">
    <ul>
      <li v-for="(item, index) in arr" :key="index">{{item}}</li>
    </ul>
    <ms-button :buttons="buttons"></ms-button>
  </div>
</template>

<script>
  import MsButton from '../components/common/components/MsButton.vue';

  export default {
    name: 'HelloWorld',
    components: {MsButton},
    comments: {MsButton},
    data() {
      return {
        arr: ['a', 'b', 'c', 'd'],
        buttons: [
          {tip: 'push', exec: this.doPush},
          {tip: 'pop', exec: this.doPop},
          {tip: 'shift', exec: this.doShift},
          {tip: 'unshift', exec: this.doUnShift},
          {tip: 'splice', exec: this.doSplice},
          {tip: 'sort', exec: this.doSort},
          {tip: 'reverse', exec: this.doReverse},
          {tip: 'index', exec: this.doIndex},
        ]
      }
    },
    methods: {
      doPush() {
        this.arr.push('e');
      },
      doPop() {
        this.arr.pop();
      },
      doShift() {
        this.arr.shift();
      },
      doUnShift() {
        this.arr.unshift('f');
      },
      doSplice() {
        this.arr.splice(0, 0, 'v');
      },
      doSort() {
        this.arr.sort();
      },
      doReverse() {
        this.arr.reverse();
      },
      doIndex() {
        this.arr[0] = 'index';
        console.log(this.arr)
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
