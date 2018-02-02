<template>
  <div>
    <stepbar :steps="steps" @stepClick="stepclick"></stepbar>  

    <button @click="backward"> Backward </button>
    <button @click="forward"> Forward </button>
    <button @click="fail"> Fail  </button>

    <div>
      <h2>
        Click on :{{message}}
      </h2>
    </div>
  </div> 
</template>

<script>

import StepBar from './StepBar.vue'
export default {
  name: 'HelloWorld',
  components:{
    'stepbar': StepBar
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      steps: [
      {id:1,'title': 'Step 1','completed':true,'active':true,'failed':false},
      {id:2,'title': 'Step 2','completed':false,'active':false,'failed':false},
      {id:3,'title': 'Step 3','completed':false,'active':false,'failed':false},
      {id:4,'title': 'Step 4','completed':false,'active':false,'failed':false},
      {id:5,'title': 'Step 5','completed':false,'active':false,'failed':false},
      {id:7,'title': 'Step 10','completed':false,'active':false,'failed':false},
      {id:8,'title': 'Step 11','completed':false,'active':false,'failed':false},
      {id:8,'title': 'Step 11','completed':false,'active':false,'failed':false},
      {id:8,'title': 'Step 11','completed':false,'active':false,'failed':false},
      {id:8,'title': 'Step 11','completed':false,'active':false,'failed':false},
      {id:8,'title': 'Step 11','completed':false,'active':false,'failed':false},
      {id:8,'title': 'Step 11','completed':false,'active':false,'failed':false},
      {id:8,'title': 'Step 11','completed':false,'active':false,'failed':false},
      {id:8,'title': 'Step 11','completed':false,'active':false,'failed':false},
      {id:8,'title': 'Step 11','completed':false,'active':false,'failed':false},
      {id:8,'title': 'Step 11','completed':false,'active':false,'failed':false},
      {id:8,'title': 'Step 11','completed':false,'active':false,'failed':false},
      {id:8,'title': 'Step 11','completed':false,'active':false,'failed':false},
      {id:8,'title': 'Step 11','completed':false,'active':false,'failed':false},
      {id:8,'title': 'Step 11','completed':false,'active':false,'failed':false},
      {id:8,'title': 'Step 11','completed':false,'active':false,'failed':false},
      {id:8,'title': 'Step 11','completed':false,'active':false,'failed':false},
      {id:8,'title': 'Step 11','completed':false,'active':false,'failed':false},
      {id:8,'title': 'Step 11','completed':false,'active':false,'failed':false},
      {id:8,'title': 'Step 11','completed':false,'active':false,'failed':false},
      {id:8,'title': 'Step 11','completed':false,'active':false,'failed':false},
      {id:8,'title': 'Step 11','completed':false,'active':false,'failed':false},
      {id:8,'title': 'Step 11','completed':false,'active':false,'failed':false},
      {id:8,'title': 'Step 11','completed':false,'active':false,'failed':false},
      {id:8,'title': 'Step 11','completed':false,'active':false,'failed':false},
      {id:8,'title': 'Step 11','completed':false,'active':false,'failed':false},
      ],
      active:1,
      message:""
    }
  },
  methods:{
    forward:function(){
      this.active ++;
      this.steps[this.active].active=true
      this.steps[this.active].completed=false
      this.steps[this.active-1].active=false
      this.steps[this.active-1].completed=true
    },
      backward:function(){
      this.active --;
      this.steps[this.active].active=true
      this.steps[this.active].completed=false
      this.steps[this.active+1].active=false
      this.steps[this.active+1].completed=false
    },
    fail:function(){
      this.steps[this.active].failed=true
      this.steps[this.active].active=false
      this.steps[this.active].completed=false
    },
    stepclick:function(step){
      this.message = step.title
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
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
