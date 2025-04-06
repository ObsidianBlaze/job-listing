<script>
  export default{
    data() {
      return{
        name : "John Doe",
        status: 'pending',
        tasks: ['Task One', 'Task Two', 'Task Three'],
        link: 'https://google.com',
      }
    }
  }
</script>

<template>
  <h1>{{ name }}, How are you</h1>
  <p v-if="status === 'active'"> User is active</p>
  <p v-else-if="status === 'pending'"> User is pending</p>
  <p v-else> User is inactive</p>

  <h3>Tasks:</h3>
  <ul>
    <li v-for="task in tasks" :key="task"> {{ task }}</li>
  </ul>
  <!-- <a v-bind:href="link">Click here for Google.</a> -->
  <a :href="link">Click here for Google.</a>
</template>
