<template>
  <div class="card">
    <h2>Message: {{  message }}</h2>
    <h2>Number: {{  number }}</h2>
    <button @click="changeMessageToUpperCase">
      Change Message to Upper Case
    </button>
    <button @click="incrementNumber">Increment Number</button>
  </div>
  <div class="card">
    <h2>Name: {{ wizard.name }}</h2>
    <h2>Wand: {{  wizard.wand }}</h2>
    <button @click="changeNameToUpperCase">Change Name to upper case</button>
    <button @click="changeWandCore">Change Name to wand core</button>
    <button @click="changeWizard">Change Name wizard</button>
  </div>
  <div class="card">
    <h2>Array: {{  wizards }}</h2>
    <button @click="wizards.push('Draco')">Add a new wizard</button>
  </div>
</template>

<script setup>
import {ref} from 'vue'
let message = ref('Hello, Reactivity!')
let number = ref(1)

function changeMessageToUpperCase() {
  message.value = message.value.toUpperCase()
  message.value
  console.log(message)
}
function incrementNumber() {
  number.value += 1
  console.log(number)
}

let wizard = ref({
  id: 1001,
  name: 'Harry Potter',
  house: 'Gryffindor',
  age: 17,
  wand: {
    wood: 'Holly',
    core: 'Phoenix Feather',
  }
})

function changeNameToUpperCase() {
  wizard.value.name = wizard.value.name.toUpperCase()
}

function changeWandCore() {
  wizard.value.wand.core = 'Unicorn Hair'
}

function changeWizard() {
  wizard.value = {
    id: 1002,
    name: 'Hermione Granger',
    house: 'Gryffindor',
    age: 17,
    wand: {
      wood: 'Vine',
      core: 'Dragon Heartstring',
    }
  }
}

let wizards = ref(['Harry', 'Hermione', 'Ron'])
</script>

<style scoped>
.card {
  background-color: purple;
  color: white;
  padding: 20px 10px;
  margin-bottom: 10px;
}
</style>