<template>
  <v-text-field
    :the-rules="theRules"
    :rules="theRules"
    :label="label"
  />
</template>

<script>

export default {
  name: 'TextField',
  props: {
    label: {
      type: String,
      default: ''
    },
    theRules: {
      type: Array,
      default: () => {}
    }
  }
}
</script>
