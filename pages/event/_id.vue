<template>
    <div>
        <h1> Event #{{ id }}</h1>
    </div>
</template>

<script>
    export default {
        head() { // <-- property used by vue-meta to add header tags
            return {
            title: 'Event # ' + this.id, // <-- For our title tag
            meta: [
                    {
                    hid: 'description event #' + this.id,  
                    name: 'description event #' + this.id, // <-- for our meta description tag
                    content:
                        'here you can see the description of the event #' + this.id
                    }
                ]
            }
        },
        computed: {
            id() { return this.$route.params.id } 
        }
    }
</script>

<style lang="scss" scoped>

</style>