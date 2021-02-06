<template>
  <p>Reaction time: {{ score }}ms</p>
  <p class="comment">{{ comment }}</p>
</template>

<script>
export default {
    props: ['score'],
    data() {
        return {
            comment: null
        }
    },
    mounted() {
        if (this.score < 250) {
            this.comment = 'ร.... เร็ว!'
        } else if (this.score < 500) {
            this.comment = 'ก็ไม่เลวเลยนี่'
        } else {
            this.comment = 'กากจังเลยอ่ะ'
        }
    }
}
</script>

<style>
.comment {
    font-size: 1.4em;
    font-weight: bold;
}
</style>