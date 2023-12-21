<template>
  <div class="about">
    <h1>This is an about page</h1>
<Card></Card>
<Hello></Hello>
  </div>
</template>
<script>
import Card from '@/components/Card.vue';
import Hello from '@/components/Hello.vue';

export default {
  components: {
    Card,
    Hello,
  },
};
</script>
