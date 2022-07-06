<script setup>
import { ref, defineProps, onMounted } from 'vue'
import moment from "moment-timezone"


const props = defineProps({
    locationName: String,
    locationSpecified: String,
    to: String,
})

const locationName = ref(props.locationName)
const currentTime = ref(props.to != undefined ? moment().tz(props.locationSpecified).format("HH:mm") +" - "+ moment().tz(props.to).format("HH:mm") : moment().tz(props.locationSpecified).format("HH:mm"))
const early = ref(false)

onMounted(() => {
  const time = (currentTime.value[0] + currentTime.value[1]).replaceAll("0", "")

  console.log(time)

  if(Number(time) < 10){
    early.value = true
  }
})
</script>

<template>
  <div
    class="bg-slate-800 text-white font-bold text-xl w-96 p-6 rounded-md flex justify-between m-3 shadow-md"
  >
    <span>{{locationName}}</span>
    <span :class="{'text-green-400' : early}">{{currentTime}}</span>
  </div>
</template>
