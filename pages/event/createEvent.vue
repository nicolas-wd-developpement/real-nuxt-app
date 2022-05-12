<template>
  <div>
    <h1>Create anEvent</h1>
  </div>
</template>

<script >
  import Vue from 'vue'

  export default Vue.extend({
    head() { // <-- property used by vue-meta to add header tags
        return {
        title: 'Event create', // <-- For our title tag
        meta: [
                {
                hid: 'description',  
                name: 'description', // <-- for our meta description tag
                content:
                    'Where you can create all the events taking place in your neighborhood'
                }
            ]
        }
    }
  })
</script>

<style>

</style>