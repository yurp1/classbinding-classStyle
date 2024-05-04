<template>
  <div>
    <h1>KATAKAN SESUATU !</h1>
    <input type="text" v-model="message" />
    <button v-on:click="sayHello">Say</button>
    <div :class="classes" :style="{ backgroundColor: bgColor }">
      {{ message }}
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isActive: true,
      isBold: false,
      bgColor: 'yellow',
      message: 'Hello World!'
    }
  },
  computed: {
    classes() {
      return {
        active: this.isActive,
        'text-bold': this.isBold
      }
    }
  },
  methods: {
    sayHello() {
      alert('Hello, ' + this.message);
    }
  }
}
</script>