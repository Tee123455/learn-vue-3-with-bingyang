<template>
<h1>message: {{ message }} </h1>
  <hr> 
<h1>number: {{ number }}</h1>
<hr>
<h1>doubleNum(50): {{ doubleNum(50) }}</h1>
<hr>
<h1>mumber *2 = {{ number *2 }}</h1>
<hr>
<h1>{{ number > 150? 'Number is greater than 150' : 'Number is less than 150' }}</h1>
<hr/>
<h1 v-text="number"></h1>
</hr>
<h1>{{ harry }}  </h1>
<h1>{{ harry.name }}  </h1>

<hr/>
<h1>{{ hogwardsWizard }}</h1>
<h1>{{ hogwardsWizard[0]}}</h1>
<hr/>

<h1>{{ rawHtml }}</h1>
<h1 v-text="rawHtml"></h1>
<h1 v-html="rawHtml"></h1>
</template>

<script setup>

let message = 'Hello, Vue'
let number = 50

function doubleNum(num) {
}

let harry = {
  id: 1001,
  name: 'Harry Potter',
  house: 'Gryffindor',
  age: 17,
  wand: {
    core: 'Phoenix feather',
    wood: 'Holly',
  }
}

const hogwardsWizard = [
  {
  id: 1001,
  name: 'Harry Potter',
  house: 'Gryffindor',
  age: 17,
  wand: {
    core: 'Phoenix feather',
    wood: 'Holly',
  }
},
{
  id: 1002,
  name: 'Hermione Granger',
  house: 'Gryffindor',
  age: 17,
  wand: {
    core: 'Dragon heartstring',
    wood: 'Vine',
  }
},
{
  id: 1003,
  name: 'Ron Weasley',
  house: 'Gryffindor',
  age: 17,
  wand: {
    core: 'Unicorn hair',
    wood: 'Willow',
  }
},
{
  id: 1004,
  name: 'Draco Malfoy',
  house: 'Slytherin',
  age: 17,
  wand: {
    core: 'Dragon heartstring',
    wood: 'Hawthorn',
  }
}
]

let rawHtml='<span style="color: red;">This is red</span>'
</script>

<style lang="scss" scoped>

</style>