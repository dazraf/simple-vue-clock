<template>
  <div class="clock">
    {{ time }}
  </div>
</template>

<script>
import moment from 'moment';

export default {
  name: 'Clock',
  data: function() {
    return {
      time: moment().format('LTS')
    }
  },
  mounted: function() {
    setInterval(()=>{
			this.time = moment().format('LTS')
		},1000)
  }
}
</script>

<style>
.clock {
  font-size: 40px;
}
</style>
