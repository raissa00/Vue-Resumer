<template>
  <div>
    <Topbar/>
    <main>
      <Editor/>
      <Preview/>
    </main>
    
  </div>
</template>

<script>
import Topbar from './components/Topbar'
import Editor from './components/Editor'
import Preview from './components/Preview'

export default {
  name: 'App',
  components: {
    Topbar,
    Editor,
    Preview
  }
}
</script>

<style>
#app {
 -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  
  
}
#app>div {
  border:1px solid red;
}

main {
  display: flex;
  flex-direction: row;

 
}
main > #editor {
    width: 500px;
  }
</style>
