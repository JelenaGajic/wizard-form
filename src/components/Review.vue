<template>
  <div class="home">
    <h3>Contact Info</h3>
    <p>{{ contactInfo.name }}</p>
    <p>{{ contactInfo.email }}</p>
    <p>{{ contactInfo.phone }}</p>
  </div>
  <div>
    <h3>Shipping Info</h3>
    <p>{{ shippingInfo.street }}</p>
    <p>{{ shippingInfo.state }}</p>
    <p>{{ shippingInfo.zip }}</p>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'Review',
  props: {
    contactInfo: Object,
    shippingInfo: Object
  }
}
</script>
