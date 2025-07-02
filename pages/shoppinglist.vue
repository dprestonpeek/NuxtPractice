<script>
import { ref } from 'vue';

export default {
  data() {
      //const parentMessage = ref('Parent')
    return {
      items: [
        { message: 'butter', checked: false },
        { message: 'milk', checked: false },
        { message: 'eggs', checked: false}
      ],
      inputText: ''
    }
  },

  methods: {
    addNewItem(inputText) {
      this.items.push({ message: this.inputText, checked: false })
    },
    
    check(item) {
      item.checked = !item.checked
      if (item.message.isStrikethrough) {
        item.message.isStrikethrough = false
      }
    },

    remove(item) {
      const index = this.items.indexOf(item);
      if (index > -1) {
        this.items.splice(index, 1);
      }
    }
  }
}
</script>

<style>
.strikethrough-text {
  text-decoration:line-through;
}
</style>

<template>

  <li v-for="item in items">
    <button @click="check(item)" @contextmenu.prevent="remove(item)">☐</button>

    <span :class="{ 'strikethrough-text': item.checked }">{{ " " + item.message }}</span>
  </li>

  <br>

  <input name="itemToAdd" v-model="inputText" />
  <button @click="addNewItem('inputText')">Add Item</button>
</template>