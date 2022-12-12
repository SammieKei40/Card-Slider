<template>
  <div class="grid m-3 place-items-center">
<div class="stack">
  <div  class="w-72 h-72 card shadow-md backdrop text-primary-content inset-0 transform hover:-translate-x-30 transition duration-300">
    <div class="flex justify-end m-4 p-4">
        <button class="border rounded-lg cursor-pointer p-2 text-white" @click="sliceCard">Skip</button>
    </div>

    <div class="card-body flex text-center p-4 text-2xl">
      <p>Does it have a <br/> Certificate of Occupancy number?</p>
    </div>
  </div> 

  <div class="w-72 h-72 card backdrop2 shadow text-primary-content inset-0 transform hover:-translate-x-30 transition duration-300">
    <div class="flex justify-between m-4 p-4">
        <button class="border rounded-lg cursor-pointer p-2 text-white" @click="">Back</button>
        <button class="border rounded-lg cursor-pointer p-2 text-white" @click="sliceCard">Skip</button>
    </div>

    <div class="card-body flex text-center p-4 text-2xl">
      <p>Does it have the name of the seller written on it?</p>
    </div>
  </div> 

  <div class="w-72 h-72 card backdrop2 shadow text-primary-content inset-0 transform hover:-translate-x-30 transition duration-300">
    <div class="flex justify-between m-4 p-4">
        <button class="border rounded-lg cursor-pointer p-2 text-white" @click="">Back</button>
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
      sliceCard(e) {
        let stack = document.querySelector(".stack");

[...stack.children].reverse().forEach(i => stack.append(i));


  let card = document.querySelector(".card:nth-child");
  if (e.target !== card) return;
  card.style.animation = "translate 700ms backwards";
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
    /* opacity: 0.3; */
  }
  </style>