<template>
  <h1>Job Details</h1>
  <h4>The Description is {{ id }}</h4>
</template>

<script>
export default {
    props: ['id'],
    // data() {
    //     return {
    //         id: this.$route.params.id
    //     }
    // }
}
</script>

<style>

</style>