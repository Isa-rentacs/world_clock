<template>
    <div>{{tz}}:{{time_str}}</div>
</template>

<script>
export default {
    name: 'Clock',
    props: {
        tz: String
    },
    data: function(){
        return {
            time_str: new Date().toLocaleString("en-US", {timeZone: this.tz})
        }
    },
    mounted: function() {
        this.timer = setInterval(() => {
            this.time_string()
        }, 1000)
    },
    methods: {
        time_string: function() {
            this.time_str = new Date().toLocaleString("en-US", {timeZone: this.tz})
        }
    }
}
</script>
