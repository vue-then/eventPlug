
<template>
    <div>
        <div id="date-picker"></div>
        <div id="time-picker"></div>
    </div>
</template>

<script>
import {DatePicker,TimePicker} from '../assets/qing/qing.js';

export default {
    data(){
        return{
            date: "2013-13-13"
        }
    },
    mounted() {
        new DatePicker({
            id: 'date-picker',
            yearRange: [2000, 2020],
            lang: 'zh',
            callback: (date) => {return this.date}
        });
        new TimePicker({
            id: 'time-picker',
            lang: 'zh',
            // callback: callback,
        });
    }, 
    methods: {
        findDate(){
            console.log(this.date,'date')
        }
    }, 
}
</script>
<style lang="css" scoped>
    @import '../assets/qing/qing.css';
</style>

