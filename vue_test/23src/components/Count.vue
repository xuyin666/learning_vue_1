<template>
    <div>
        <h1>The actual sum is: {{sum}}</h1>
        <select v-model.number="n">
            <option value="1">1</option>
            <option value="2">2</option>
            <option value="3">3</option>
        </select>
        <button @click="increment">+</button>
        <button @click="decrement">-</button>
        <button @click="incrementOdd">Add if the Sum is impair</button>
        <button @click="incrementWait">Wait a little to add</button>
    </div>
</template>

<script>
export default {
    name: 'Count',
    data() {
        return {
            n: 1, // the chiffre choisi par l'utilisateur
            sum: 0 // la somme 
        }
    },
    methods: {
        increment(){
            this.sum += this.n;
        },
        decrement(){
            this.sum -= this.n;
        },
        incrementOdd(){
            if (this.sum % 2) {
                this.sum += this.n;
            }
        },
        incrementWait(){
            setTimeout(() => {
                this.sum += this.n
            }, 500)
        }
    }

}
</script>

<style scoped>
button {
    margin-left: 5px;
}


</style>