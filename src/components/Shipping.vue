<template>
  <div class="home">
    <div class="p-field">
      <label for="street-input">Street: </label>
      <InputText :value="street" @input="changeStreet" id="street-input" type="text"/>
    </div>
    <div class="p-field">
      <label for="state-input">State: </label>
      <InputText :value="state" @input="changeState" id="state-input" type="text"/>
    </div>
    <div class="p-field">
      <label for="zip-input">Zip: </label>
      <InputNumber :value="zip" @input="changeZip" id="zip-input" type="number"/>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import InputText from 'primevue/inputtext'
import InputNumber from 'primevue/inputnumber'

export default {
  name: 'Shipping',
  components: {
    InputText,
    InputNumber
  },
  props: {
    street: String,
    state: String,
    zip: Number
  },
  emits: [
    'update:street',
    'update:state',
    'update:zip'
  ],
  methods: {
    changeStreet (e) {
      this.$emit('update:street', e.target.value)
    },
    changeState (e) {
      this.$emit('update:state', e.target.value)
    },
    changeZip (e) {
      this.$emit('update:zip', e.target.value)
    },
  }
}
</script>

<style scoped>
input {
  width: 100%;
}
</style>
