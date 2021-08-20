<template>
  <div>
    <div class="card card-link py-4 mt-3">
      <span>@ {{ event.time }} on {{ event.date }}</span>
      <h4>{{ event.title }}</h4>
    </div>
  </div>
</template>

<script>
export default {
  name: "EventCard",
  props: {
    event: Object,
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
