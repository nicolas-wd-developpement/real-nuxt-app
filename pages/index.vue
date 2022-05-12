<template>
  <div>
    <h1> Event    </h1>
      <EventCard
      v-for="(event, index) in events"
      :key="index"
      :event="event"
      :data="index"
    />
  </div>
</template>

<script>
import EventCard from '../components/EventCard.vue'
export default {
      head() { // <-- property used by vue-meta to add header tags
        return {
          title: 'Event Listing', // <-- For our title tag
        }
      },
      asyncData({$axios, error}) {
              return $axios.get('http://localhost:3000/events').then(response => {
                return {
                  events: response.data
                }
              }).catch(e => { 
                error ({ 
                  statusCode: 503,
                  message: 'Unable to fetch events'
                  })
              })
            },
    component: {
      EventCard
    }
    }
</script>
