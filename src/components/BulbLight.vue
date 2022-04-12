
<script>
export default {
    props: ["necessaryClicks"],
    data() {
        return {
            cargas: this.necessaryClicks
        }
    },
    methods: {
        decrementarCargas() {
            this.cargas--;
        }
    }

}
</script>

<template>
    <div v-if="cargas > 0" @click="decrementarCargas" class="bulb bulb-off">
        <p> {{ cargas }} </p>
    </div>
    <div v-else class="bulb bulb-on"></div>
</template>

<style scoped>
p {
    font-size: 1.5rem;
    font-weight: 700;
}

.bulb {
    display: flex;
    justify-content: center;
    align-items: center;
}

.bulb-off {
    width: 265px;
    height: 400px;
    background: url('lightoff.png') no-repeat;
    margin: auto;
}

.bulb-on {
    width: 265px;
    height: 400px;
    background: url('lighton.png') no-repeat;
    ;
    margin: auto;
}
</style>