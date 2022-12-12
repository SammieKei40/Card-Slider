<template>
  <div class="grid m-3 place-items-center">
<div class="stack">
  <div  class="w-72 h-72 card shadow-md backdrop text-primary-content">
    <div class="flex justify-end m-3 p-3">
        <button class="border rounded-lg cursor-pointer p-2 text-white" @click="sliceCard">Skip</button>
    </div>

    <div class="card-body flex text-center p-4 text-2xl">
      <p>Does it have a <br/> Certificate of Occupancy number?</p>
    </div>
  </div> 

  <div class="w-72 h-72 card backdrop2 shadow text-primary-content">
    <div class="flex justify-between m-4 p-4">
        <button class="border rounded-lg cursor-pointer p-2 text-white" @click="sliceCard">Back</button>
        <button class="border rounded-lg cursor-pointer p-2 text-white" @click="sliceCard">Skip</button>
    </div>

    <div class="card-body flex text-center p-4 text-2xl">
      <p>Does it have the name of the seller written on it?</p>
    </div>
  </div> 

  <div class="w-72 h-72 card backdrop2 shadow text-primary-content">
    <div class="flex justify-between m-4 p-4">
        <button class="border rounded-lg cursor-pointer p-2 text-white" @click="sliceCard">Back</button>
        <button class="border rounded-lg cursor-pointer p-2 text-white" @click="sliceCard">Skip</button>
    </div>

    <div class="card-body flex text-center p-4 text-2xl">
      <p>Does it contain <br/> the location details?</p>
    </div>
  </div>
</div>
</div>
</template>
  
  <script>


  export default {
    data() {
      return {
      }
    },
    methods: {
      sliceCard() {
        this.$refs.card.push(this.card.shift());
      },
      removeCard() {
        // Your code for removing a card goes here
      }
    }
  }
  </script>
  

  <style scoped>
  .backdrop{
    background: linear-gradient(182.35deg, #113045 -6%, #437496 103.7%);
    border-radius: 30px;
  }
  .backdrop2{
    background: linear-gradient(182.35deg, #113045 -6%, #437496 103.7%);
    border-radius: 30px;
    opacity: 0.3;
  }
  </style>