<template>
    <v-textarea
      :label="label"
      @input="updateVar"
      v-model="ll"
      hint="Hint text"
    ></v-textarea>
</template>

<script>

export default {
    data: () => {
        return {
            ll: ''
        }
    },
    props: {
        label: String,
        targetElem: String,
        val: String
    },
    methods: {
        updateVar(e) {
            this.$store.dispatch('updateVar', [this.targetElem, this.ll])
        }
    }
}
</script>