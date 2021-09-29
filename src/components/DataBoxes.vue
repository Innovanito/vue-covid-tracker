<template>
  <div class="grid md:grid-cols-2 gap-4">
    <div class="shadow-md bg-blue-100 p-10 text-center rounded">
      <h3 class="text-3xl text-blue-900 font-bold mb-4">
        Cases
      </h3>
      <div class="text-2xl mb-4">
        <span class="font-bold">New Confirmed:</span>
        <!-- {{ numberWithCommas(stats.NewConfirmed) }} -->        
      </div>
      <div class="text-2xl mb-4">
      <span class="font-bold"> <br> Total Confirmed: </span>
        <!-- {{ numberWithCommas(stats.TotalConfirmed) }} -->
      </div>
    </div>
  </div>
  
  <div class="grid md:grid-cols-2 gap-4">
    <div class="shadow-md bg-blue-200 p-10 text-center rounded mt-10">
      <h3 class="text-3xl text-blue-900 font-bold mb-4">
        Deaths
      </h3>
      <div class="text-2xl mb-4">
        <span class="font-bold">New Deaths:</span>
        <!-- {{ numberWithCommas(stats.NewDeaths) }}         -->
      </div>
      <div class="text-2xl mb-4">
      <span class="font-bold"> <br> Total Deaths: </span>
        <!-- {{ numberWithCommas(stats.TotalDeaths) }} -->
      </div>
    </div>
  </div>

</template>

<script>
export default {
  name: 'DataBoxes',
  props: ['stats'],
  methods: {
    numberWithCommas(x) {
      // return x.toString().replace(/\B(?=(\d{3}+(?!\d))/g, ',')
    }
  }
}

</script>