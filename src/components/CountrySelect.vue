<template>
  <select 
    @change="onChange()"
    v-model="selected" 
    class="form-select mt-5 block w-full border p-3 rounded ">
    <option value="">Select Country</option>
    <option v-for="country in countries" :value="country.ID" :key="country"  >
      {{ country.Country}}
    </option>
  </select>
</template>

<script>
export default {
  name: 'CountrySelect',
  props: ['countries'],
  data() {
    return {
      selected: 0
    }
  },
  methods: {
    onChange() {
      const country = this.countries.find((item) => item.ID === this.selected)

      this.$emit('get-country')
    }
  }
}
</script>