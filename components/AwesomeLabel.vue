<template>
  <v-chip :color="color" disabled label outline small>{{ content }}</v-chip>
</template>

<script>
import colors from '@/data/colors'

export default {
  name: 'AwesomeLabel',
  props: {
    content: {
      type: String,
      required: true
    }
  },
  computed: {
    color() {
      const { content } = this
      return content in colors ? colors[content] : 'primary'
    }
  }
}
</script>
