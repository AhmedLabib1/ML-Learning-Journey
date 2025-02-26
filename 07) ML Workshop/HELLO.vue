<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Vue.js Example</title>
  <script src="https://cdn.jsdelivr.net/npm/vue@2"></script>
  <style>
    body {
      font-family: Arial, sans-serif;
      padding: 20px;
    }
    button {
      margin-top: 10px;
    }
  </style>
</head>
<body>
  <div id="app">
    <h1>{{ message }}</h1>
    <p>Count: {{ count }}</p>
    <button @click="incrementCount">Click me!</button>
    <p v-if="count > 0">You clicked the button {{ count }} times!</p>
  </div>

  <script>
    // Create a new Vue instance
    new Vue({
      el: '#app',
      data: {
        message: 'Welcome to Vue.js!',
        count: 0
      },
      methods: {
        incrementCount() {
          this.count++;
        }
      }
    });
  </script>
</body>
</html>
