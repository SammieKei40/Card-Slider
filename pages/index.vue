<template>
<div class="container mx-auto min-h-screen justify-center items-center">

  <div class="flex border rounded-full bg-blue-100 p-8 m-4 justify-around">
    <h1>Survey Plan</h1>
    <div class="ml-20 w-52 h-8 bg-blue-100 rounded-full">
        <div ref="myBar" class="progress  h-8 rounded-full text-xs font-medium text-blue-100 text-center p-2 leading-none" style="width:0%">In Progress</div>
    </div>

    <!-- <div class="w-full bg-gray-200 h-5 mb-6">
  <div class="bg-blue-600 h-5" style="width: 25%"></div>
</div> -->
  </div>  
  

    <!-- Card -->
    <div card-stack class="">
    <p class="text-center m-2">Swipe left/right to the next question</p>
    <input id="card-0" name="card-set" type="radio" checked />
    <div card class="backdrop2 overflow-hidden">
        <div class="content">
            <div class="flex justify-end mb-8 p-4 ">
                <label for="card-1" class="border rounded-lg cursor-pointer p-2 text-white" @click="move">Skip</label>
            </div>

            <div class="card-body flex text-center text-white p-4 ">
                <p class="text-2xl">Does it contain the <br /> name of the owner of the property with no <br /> mistake?</p>
                <p class="mt-10 text-sm">1/10</p>
            </div>
        </div>
    </div>

    <input id="card-1" name="card-set" type="radio" />
    <div card class="backdrop2">
        <div class="content">
            <div class="flex justify-between mb-8 p-4 ">
                <label for="card-0" class="border rounded cursor-pointer p-1 text-white">Back</label>
                <label for="card-2" class="border rounded cursor-pointer p-1 text-white">Skip</label>
            </div>

            <div class="card-body flex text-center text-white p-4 ">
                <p class="text-2xl">Does the survey plan contain the name of the street and the name of the area including the Local government?</p>
                <p class="mt-5 text-sm">2/10</p>
            </div>
        </div>
    </div>

    <input id="card-2" name="card-set" type="radio" />
    <div card class="backdrop2">
        <div class="content">
            <div class="flex justify-between mb-8 p-4 ">
                <label for="card-1" class="border rounded cursor-pointer p-1 text-white">Back</label>
                <label for="card-3" class="border rounded cursor-pointer p-1 text-white">Skip</label>
            </div>

            <div class="card-body flex text-center text-white p-4 ">
                <p class="text-2xl">Does it contain the size of the land surveyed?</p>
                <p class="mt-10 text-sm">3/10</p>
            </div>
        </div>
    </div>

    <input id="card-3" name="card-set" type="radio" />
    <div card class="backdrop2">
        <div class="content">
            <div class="flex justify-between mb-8 p-4 ">
                <label for="card-2" class="border rounded cursor-pointer p-1 text-white">Back</label>
                <label for="card-4" class="border rounded cursor-pointer p-1 text-white">Skip</label>
            </div>

            <div class="card-body flex text-center text-white p-4 ">
                <p class="text-2xl">Does it show the survey plan number?</p>
                <p class="mt-10 text-sm">4/10</p>
            </div>
        </div>
    </div>

    <input id="card-4" name="card-set" type="radio" />
    <div card class="backdrop2">
        <div class="content">
            <div class="flex justify-between mb-8 p-4 ">
                <label for="card-3" class="border rounded cursor-pointer p-1 text-white">Back</label>
                <label for="card-5" class="border rounded cursor-pointer p-1 text-white">Skip</label>
            </div>

            <div class="card-body flex text-center text-white p-4 ">
                <p class="text-2xl">Does it have a stamp showing that the land is free from the government?</p>
                <p class="mt-10 text-sm">5/10</p>
            </div>
        </div>
    </div>

    <input id="card-5" name="card-set" type="radio" />
    <div card class="backdrop2">
        <div class="content">
            <div class="flex justify-between mb-8 p-4 ">
                <label for="card-4" class="border rounded cursor-pointer p-1 text-white">Back</label>
                <label for="card-6" class="border rounded cursor-pointer p-1 text-white">Skip</label>
            </div>

            <div class="card-body flex text-center text-white p-4 ">
                <p class="text-2xl">Does it hvae the date the survey plan was drawn?</p>
                <p class="mt-10 text-sm">6/10</p>
            </div>
        </div>
    </div>

    <input id="card-6" name="card-set" type="radio" />
    <div card class="backdrop2">
        <div class="content">
            <div class="flex justify-between mb-8 p-4 ">
                <label for="card-5" class="border rounded cursor-pointer p-1 text-white">Back</label>
                <label for="card-7" class="border rounded cursor-pointer p-1 text-white">Skip</label>
            </div>

            <div class="card-body flex text-center text-white p-4 ">
                <p class="text-2xl">Does it have a drawn out portion of the land survey and mapped out on the survey document?</p>
                <p class="mt-10 text-sm">7/10</p>
            </div>
        </div>
    </div>

    <input id="card-7" name="card-set" type="radio" />
    <div card class="backdrop2">
        <div class="content">
            <div class="flex justify-between mb-8 p-4 ">
                <label for="card-6" class="border rounded cursor-pointer p-1 text-white">Back</label>
                <label for="card-8" class="border rounded cursor-pointer p-1 text-white">Skip</label>
            </div>

            <div class="card-body flex text-center text-white p-4 ">
                <p class="text-2xl">Does it have the name, signature and logo of the surveyor who drew the plan?</p>
                <p class="mt-10 text-sm">8/10</p>
            </div>
        </div>
    </div>

    <input id="card-8" name="card-set" type="radio" />
    <div card class="backdrop2">
        <div class="content">
            <div class="flex justify-between mb-8 p-4 ">
                <label for="card-7" class="border rounded cursor-pointer p-1 text-white">Back</label>
                <label for="card-9" class="border rounded cursor-pointer p-1 text-white">Skip</label>
            </div>

            <div class="card-body flex text-center text-white p-4 ">
                <p class="text-2xl">Does it have the registered seal of the surveyor?</p>
                <p class="mt-10 text-sm">9/10</p>
            </div>
        </div>
    </div>

    <input id="card-9" name="card-set" type="radio" />
    <div card class="backdrop2">
        <div class="content">
            <div class="flex justify-between mb-8 p-4 ">
                <label for="card-8" class="border rounded cursor-pointer p-1 text-white">Back</label>
            </div>

            <div class="card-body flex text-center text-white p-4 ">
                <p class="text-2xl">Does it have beacon numbers?</p>
                <p class="mt-10 text-sm">10/10</p>
            </div>
        </div>
    </div>

</div>
</div>
</template>
  
<script>
export default {
  data() {
    return {
  
    };
  },
  methods: {
 move() {
    var elem = this.$refs.myBar
var width = 0;
var id = null;
var click = false;
if(!click){
  click = true;
  id = setInterval(function() {
    width++;
    if (width > 100) ;
    if (width % 100 === 0){
    clearInterval(id);
    click = false;
    }
    elem.style.width = width + '%';
    elem.innerHTML = width * 1 + '%';
  }, 30);
}

}
   },
};
</script> 

  <style>
    .progress{
    background: linear-gradient(182.35deg, #113045 -6%, #437496 103.7%)
  }
  .backdrop2{
    background: linear-gradient(182.35deg, #113045 -6%, #437496 103.7%);
    border-radius: 30px;
    opacity: 0.3;
  }

  [card-stack] {
    will-change: transform;
    position: relative;
    width: 20rem;
    margin: auto;
    margin-top: 2rem;
}
[name="card-set"] {
    display: none;
}
[name="card-set"]:checked+[card] {
    display: flex;
    opacity: 1;
    filter: blur(0);
    transform: translateY(0) scale(1);
    transition: transform 1s, opacity 1s, filter 0.25s;
    transition-delay: 0.3s;
    z-index: 0;
}
[name="card-set"]:checked+[card]~[card] {
    z-index: -1;
    display: flex;
    opacity: 0.1;
    filter: blur(1px);
    transform:  translateY(1.2rem) scale(0.95);
    transition: transform 1.5s, opacity 1.5s, filter 0.5s;
    transition-delay: 0.4s;
}
[name="card-set"]:checked+[card]~[card]~[card] {
    z-index: -2;
    display: flex;
    opacity: 0.2;
    filter: blur(2px);
    transform: translateY(2.4rem) scale(0.9);
    transition: transform 2s, opacity 2s, filter 1.5s;
    transition-delay: 0.5s;
}
[name="card-set"]:checked+[card]~[card]~[card]~[card] {
    z-index: -3;
    display: flex;
    opacity: 0.2;
    filter: blur(3px);
    transform: translateY(3.6rem) scale(0.85);
    transition: transform 2.5s, opacity 2.5s, filter 2s;
    transition-delay: 0.7s;
}
[name="card-set"]:checked+[card]~[card]~[card]~[card]~[card] {
    z-index: -4;
    display: flex;
    opacity: 0;
    filter: blur(4px);
    transform: translateY(5rem) scale(0.7);
    transition: transform 3s, opacity 3s, filter 2.5s;
    transition-delay: 0.8s;
}

[name="card-set"]:checked+[card]~[card]~[card]~[card]~[card]~[card] {
    z-index: -5;
    display: flex;
    filter: blur(5px);
    transform: translateY(5rem) scale(0..65);
    transition: transform 3s, opacity 3s, filter 2.5s;
    transition-delay: 0.8s;
}

[name="card-set"]:checked+[card]~[card]~[card]~[card]~[card]~[card]~[card]{
    z-index: -6;
    display: flex;
    filter: blur(6px);
    transform: translateY(5rem) scale(0.0.5);
    transition: transform 3s, opacity 3s, filter 2.5s;
    transition-delay: 0.8s;
}

[card] {
    display: flex;
    will-change: filter opacity transform;
    position: absolute;
    width: 100%;
    background-color: white;
    opacity: 0;
    transform: translateY(0) translateX(calc(-100% - 1rem)) scale(1);
    transition: transform 0.5s, opacity 0.2s 0.3s, filter 0.1s;
    transition-timing-function: ease-in;
    box-shadow: 0 0.2rem 0 rgba(0, 0, 0, .2);
    justify-content: center;
    align-items: center;
    z-index: 1;
    height: auto;
}
[card]::before {
    content: '';
    display: block;
    padding-bottom: 130%;
}
[card] .content {
    /* flex-direction: column;
    align-items: center;
    justify-content: space-around;
    padding: 2rem;
    text-align: center; */
    margin-top: -4%;
}
[card] label {
    color: white;
    display: inline-block;
    user-select: none;
}
</style>