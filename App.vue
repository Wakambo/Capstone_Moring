<template>
  <div id="app">
    <input 
      type="text" 
      v-model="message" 
      placeholder="Start typing here..." 
      class="text-input"
    >

    <p class="display-text">
      **Live Preview:** {{ message }}
    </p>

    <small>
      Character Count: {{ message.length }}
    </small>
  </div>
</template>

<script>
// Options API component export (as used in the original example)
export default {
  name: 'InputDisplay',
  
  // The 'data' function defines the initial reactive state for the component.
  data() {
    return {
      // 'message' is the reactive data property used by v-model.
      message: ''
    }
  }
}
</script>

<style>
/* Optional styling for basic presentation */
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 8px;
  max-width: 400px;
  margin-left: auto;
  margin-right: auto;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.text-input {
  width: 100%;
  padding: 10px;
  margin-bottom: 20px;
  border: 2px solid #42b983; /* Vue Green */
  border-radius: 4px;
}

.display-text {
  padding: 15px;
  background-color: #f0fff4; 
  border-left: 5px solid #42b983;
  text-align: left;
  font-size: 18px;
  word-break: break-word; 
  min-height: 40px; 
}
</style>
