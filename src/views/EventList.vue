<template>
  <div class="container">
    <h1>Events For Good</h1>
    <div class="row justify-content-center">
      <div class="col-md-6">
        <EventCard v-for="event in events" :key="event.id" :event="event" />
      </div>
    </div>
  </div>
</template>

<script>
import EventCard from "@/components/EventCard.vue"
import EventService from '@/services/EventService.js'

export default {
  name: "EventList",
  components: {
    EventCard,
  },
  data() {
    return {
      events: null,
    }
  },
  created() {
    EventService.getEvents()
      .then(response => {
        this.events = response.data
      })
      .catch(error => {
        console.log(error)
      })
  }
};
</script>
