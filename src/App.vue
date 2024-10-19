<template>
  <SignupForm v-if="showSignupForm" />
  <ReactionTimer v-if="showReactionTimer" />
  <button @click="toggleSignupForm">Show Signup Form</button>
  <button @click="toggleReactionTimer">Show Reaction Timer</button>
</template>

<script>
import SignupForm from './components/SignupForm.vue'
import ReactionTimer from './components/ReactionTimer.vue'

export default {
  name: 'App',
  components: {
    SignupForm,
    ReactionTimer
  },
  data() {
      return {
          showSignupForm: false,
          showReactionTimer: false
      }
  },
  methods: {
    toggleSignupForm() {
        this.showSignupForm = !this.showSignupForm
    },
    toggleReactionTimer() {
      this.showReactionTimer = !this.showReactionTimer
    }
  }

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
