<script>
export default {
  data() {
    return {
      message: "Hello Vue js",
      count: 0,
      name: "",
      users: ["sardor", "hojiakbar", "jumavoy", "tursunqul"],
      image:
        "https://img-cdn.pixlr.com/image-generator/history/65bb506dcb310754719cf81f/ede935de-1138-4f66-8ed7-44bd16efc709/medium.webp",
      arr: [],
    };
  },
  methods: {
    increment() {
      this.count++;
    },
    addInput() {
      if (this.name.trim() =="") return;
      this.arr.push(this.name);
    },
  },
};
</script>

<template>
  <!-- <div>
    <h1>{{ message }}</h1>
    <input type="text" v-model="name" />
    <h2 v-if="name.length > 10">v-if:{{ name }}</h2>
    <h2 v-else-if="name.length > 5">v-else-if: {{ name }}</h2>
    <h2 v-else>v-else: {{ name }}</h2>

    <h3 v-show="name.length > 10">v-show: {{ name }}</h3>

    <h1 v-once>{{ count }}</h1>

    <button @click="increment">count: {{ count }}</button>

    <ul>
      <li v-for="(item, index) in users" :key="index">{{ item }}</li>
    </ul>

    <img :src="image" alt="" />

    <h1 :class="{ active: name.length > 10 }">Binding class</h1>
  </div> -->
  <!-- <HelloWorld msg="Vite + Vue" /> -->
  <div>
    <input type="text" v-model="name" class="input" @keyup.enter="addInput"/>
    <button @click="addInput">Send</button>
    <ul>
      <li v-for="(item, index) in arr" :key="index">{{ item }}</li>
    </ul>
  </div>
</template>

<style scoped>
.active {
  font-size: 30px;
  color: red;
}
.input {
  margin-right: 10px;
  height: 30px;
}
</style>
