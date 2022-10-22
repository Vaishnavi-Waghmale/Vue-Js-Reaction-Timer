<template>
    <div id="result">
        <p>Reaction Time - {{score}} ms</p>
        <p class="rank">{{rank}}</p>
    </div>


</template>


<script>

export default {
    props: ['score'],
    data() {
        return {
            rank: null
        }
    },
    mounted() {
        if (this.score < 250) {
            this.rank = 'Great Reflexes'
        }
        else if (this.score < 400) {
            this.rank = 'Good job, quite fast'
        }
        else if (this.score < 1000) {
            this.rank = 'Nicely done!'
        }
        else {
            this.rank = 'Ohh You need to be attentive'
        }
    }
}

</script>


<style>
#result {
    width: 400px;
    border-radius: 20px;
    background: rgb(46, 1, 8);
    color: white;
    text-align: center;
    padding: 100px 0;
    margin: 40px auto;
}

.rank {
    font-size: 1.4em;
    font-weight: bold;
}
</style>