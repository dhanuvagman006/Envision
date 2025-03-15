<script>
export default{
  data(){
    return{
      name:"Yeah I Did It!",
      status:'pending',
      tasks:["Hello","World"],
      skills:["Python","CPP","Vue","JS"],
      link:"https://www.google.com"
    }
  },
  methods:{
    togglests(){
      if(this.status==='active'){
        this.status='pending';
      }else if(this.status==='pending'){
        this.status='active'
      }
    }
  }
}
</script>

<template>
  <h1>{{ name }}</h1>
  <h2 v-if="status==='active'">User is ALive</h2>
  <h2 v-else-if="status==='pending'">User is half dead</h2>
  <h2 v-else>User is Dead</h2><br>
  <h3>Task Lists:</h3>
  <p v-for="task in tasks":key='task'>{{ task }}</p>
  <p v-for="sk in skills":key='sk'>{{ sk }}</p>
  <a :href="link">Click For Google</a>
   <button @click="togglests">Click me to Bring User Back Live!</button>
</template>
