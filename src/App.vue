<template>
  <Clock tz="PST"/>
  <Clock tz="UTC"/>
  <Clock tz="JST"/>
  <Clock tz="EST"/>
  <Clock tz="CET"/>
  <Clock tz="IST"/>
</template>

<script>
import Clock from './components/Clock.vue'

export default {
  name: 'App',
  components: {
    Clock
  }
}
</script>
