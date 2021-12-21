<template>
  <component>
    <h3>{{product.name}}</h3>
    <p>{{product.short_name}}</p>
  </component>
</template>

<script>
export default {
  props: {
    product: {
      type: Object, 
      default: () => {
      }
    }
  }
}
</script>
