<template>
    <div class="text-center">
        <h2 class="text 3-xl font-bold">{{text}}</h2>
        <div class="text-2xl mt-4 mb-10">
            {{timestamp}}
        </div>
    </div>
</template>

<script>

import moment from 'moment'

    export default{
        name:'DateTitle',
        props:['text','dataDate'],
        computed:{
            timestamp: function(){
                return moment(this.dataDate).format('MMMM Do YYYY, h:mm:ss a')
            },
        },
    }
</script>
