<template>
  <div id="home">
    <img src="../assets/logo.png">

    <!-- The navigation menu will get the value of the "active" variable as a class. -->

    <!-- To stops the page from jumping when a link is clicked 
        we use the "prevent" modifier (short for preventDefault). -->

    <nav v-bind:class="active" v-on:click.prevent>

        <!-- When a link in the menu is clicked, we call the makeActive method, 
        defined in the JavaScript Vue instance. It will change the value of "active". -->

	<ul style="list-style-type:none">
          <li> <a href="#" class="home" v-on:click="makeActive('home')">Home</a> </li>
          <li> <a href="#" class="home" v-on:click="makeActive('home')">Home</a> </li>
          <li> <a href="#" class="projects" v-on:click="makeActive('projects')">Projects</a> </li>
          <li> <a href="#" class="services" v-on:click="makeActive('services')">Services</a> </li>
          <li> <a href="#" class="contact" v-on:click="makeActive('contact')">Contact</a> </li>
        </ul>
    </nav>

    <!-- The mustache expression will be replaced with the value of "active".
         It will automatically update to reflect any changes. -->

    <p>You chose <b>{{active}}</b></p>
  </div>
</template>

<script>
export default {
  name: 'home',
  methods: {
    makeActive: function (item) {
      // When a model is changed, the view will be automatically update
      this.active = item
    }
  },
  data () {
    return {
      active: 'Welcome to Your Vue.js App'
    }
  }
}
</script>
<!-- styling for the component -->
<style>
#about {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #2c3e50;
  margin-top: 20px;
}
</style>
