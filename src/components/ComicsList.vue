<template>
    <div>
        <h2>comics list</h2>
        <ComicCard></ComicCard>
    </div>
</template>


<script>
import ComicCard from './ComicCard.vue';

export default {
  name: 'ComicsList',
  components: {
    // Demo,
    ComicCard,
  },
}
</script>

<style>

</style>