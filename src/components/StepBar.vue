<template>
    <div>
<ol class="progress">
    <li v-for="(step,index) in steps" :data-step="index" :class="{ 'is-active' : step.active,'is-complete' : step.completed }">
        {{step.title}}
    </li>
</ol>
    </div>
</template>

<script>
export default {
  data: function () {
    return {
      steps: [
      {id:'ST1','title': 'Step 1',completed:true,active:false},
      {id:'ST2','title': 'Step 2',completed:true,active:false},
      {id:'ST3','title': 'Step 3',completed:true,active:false},
      {id:'ST4','title': 'Step 4',completed:false,active:true},
      {id:'ST5','title': 'Step 5',completed:false,active:false},
      {id:'ST6','title': 'Step 6',completed:false,active:false},
      {id:'ST7','title': 'Step 6',completed:false,active:false},
      {id:'ST8','title': 'Step 7',completed:false,active:false},
      {id:'ST9','title': 'Step 8',completed:false,active:false},
      {id:'ST10','title': 'Step 9',completed:false,active:false},
      {id:'ST11','title': 'Step 10',completed:false,active:false},
      {id:'ST12','title': 'Step 11',completed:false,active:false},
      ]
    }
  }
}
</script>

<style scoped>
.progress {
  list-style: none;
  margin: 0;
  padding: 0;
  display: table;
  table-layout: fixed;
  width: 100%;
  color: #849397;
}
.progress > li {
  position: relative;
  display: table-cell;
  text-align: center;
  font-size: 0.8em;
}
.progress > li:before {
  content: attr(data-step);
  display: block;
  margin: 0 auto;
  background: #DFE3E4;
  width: 3em;
  height: 3em;
  text-align: center;
  margin-bottom: 0.25em;
  line-height: 3em;
  border-radius: 100%;
  position: relative;
  z-index: 1000;
}
.progress > li:after {
  content: '';
  position: absolute;
  display: block;
  background: #DFE3E4;
  width: 100%;
  height: 0.5em;
  top: 1.25em;
  left: 50%;
  margin-left: 1.5em\9;
  z-index: -1;
}
.progress > li:last-child:after {
  display: none;
}
.progress > li.is-complete {
  color: #2ECC71;
}
.progress > li.is-complete:before, .progress > li.is-complete:after {
  color: #FFF;
  background: #2ECC71;
}
.progress > li.is-active {
  color: #3498DB;
}
.progress > li.is-active:before {
  color: #FFF;
  background: #3498DB;
}

/**
 * Needed for IE8
 */
.progress__last:after {
  display: none !important;
}

/**
 * Size Extensions
 */
.progress--medium {
  font-size: 1.5em;
}

.progress--large {
  font-size: 2em;
}

/**
 * Some Generic Stylings
 */
*, *:after, *:before {
  box-sizing: border-box;
}

h1 {
  margin-bottom: 1.5em;
}

.progress {
  margin-bottom: 3em;
}

a {
  color: #3498DB;
  text-decoration: none;
}
a:hover {
  text-decoration: underline;
}

body {
  text-align: center;
  color: #444;
}

</style>
