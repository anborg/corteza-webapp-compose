<template>
  <wrap v-bind="$props" v-on="$listeners">
    <automation-buttons
      class="d-flex flex-wrap"
      button-class="m-1 flex-fill"
      :buttons="options.buttons"
      v-bind="$props"
    />
  </wrap>
</template>
<script>
import base from './base'
import AutomationButtons from './Shared/AutomationButtons'

export default {
  components: { AutomationButtons },
  extends: base,

  props: {
    extraEventArgs: {
      type: Object,
      default: () => ({}),
    },
  },
}
</script>
