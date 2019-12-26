<template>
  <v-form>
    <text-field
      v-model="value"
      :the-rules="setRules()"
      :rules="setRules"
      label="Custom text field"
    />
  </v-form>
</template>

<script>
import TextField from '@/components/TextField.vue'
export default {
  components: { TextField },
  data () {
    return {
      rules: [],
      value: ''
    }
  },
  methods: {
    setRules () {
      return [this.isRequired, this.checkLength]
    },
    isRequired (v) {
      return !!v || 'The input is required'
    },
    checkLength () {
      return this.value.length > 5 || 'Should have 5 letters minimum'
    }
  }
}
</script>
