<script setup>
import TimeZone from "./TimeZone.vue";

</script>

<template>
  <div
    class="flex justify-center items-center w-screen h-screen bg-slate-500 flex-col"
  >

    <TimeZone locationName="UK" locationSpecified="Europe/London" />
    <TimeZone locationName="USA" locationSpecified="America/Los_Angeles" to="America/New_York" />
    <TimeZone locationName="Netherlands" locationSpecified="Europe/Amsterdam" />
    <TimeZone locationName="Germany" locationSpecified="Europe/Berlin" />
    <TimeZone locationName="Europe" locationSpecified="Europe/London" to="Europe/Athens"/>
    <TimeZone locationName="West-coast" locationSpecified="America/New_York" />
    <TimeZone locationName="East-coast" locationSpecified="America/Los_Angeles" />
    <TimeZone locationName="France" locationSpecified="Europe/Paris" />
    <TimeZone locationName="Texas" locationSpecified="America/Atikokan" />
  </div>
  
</template>
