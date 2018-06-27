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

<style lang="scss">




main {
  display: flex;
  flex: 1;

  > #editor {
    width: 40em;
    margin: 16px 8px 16px 16px;
    border-radius: 4px;
    background: #fff;
    overflow: hidden;    
  }
 
}

.icon {
       width: 1em; height: 1em;
       vertical-align: -0.15em;
       fill: currentColor;
       overflow: hidden;
    }
</style>
