<template>
  <div>
    <p>id: {{ id }}</p>
  </div>
</template>

<script>
export default {
  validate({ params }) {
    // only numbers are permitted
    return /^\d+$/.test(params.id)
  },
  data({ params }) {
    return {
      id: 12,
    }
  },
  mounted() {
    console.log(this.$routes)
  },
}
</script>
