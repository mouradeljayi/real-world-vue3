<template>
  <router-link class="text-decoration-none text-black" :to="{ name: 'EventDetails', params: { id: event.id } }">
    <div class="card card-link py-4 mt-3">
      <span>@ {{ event.time }} on {{ event.date }}</span>
      <h4>{{ event.title }}</h4>
    </div>
  </router-link>
</template>

<script>
export default {
  name: "EventCard",
  props: {
    event:{
      type: Object,
      required: true
    },
  },
};
</script>

<style scoped>
.card-link{
  cursor: pointer;
}
.card-link:hover {
  transform: scale(1.01);
  box-shadow: 0 3px 12px 0 rgba(0, 0, 0, 0.2);
}
</style>
