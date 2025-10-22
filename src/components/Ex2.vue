<script>
    export default { 
        // Add code in appropriate places
        data() {
            return {
                items: ['keyboard', 'mouse', 'iPhone', 'macbook', 'adapter']
            }
            
        },
        methods: {
            addItem(){
                if (this.newItem.trim()){
                    this.items.push(this.newItem)
                    this.newItem = ''
                }
            }
        }
    }
</script>

<template>

    <h2>Shopping Cart</h2>
    <!-- TODO: Add Code Here -->
        <ul id="items">
            <li v-for="item in items">{{ item }}<button @click=$event.target.parentElement.remove()>Delete!</button></li>
        </ul>
    <input type="text" v-model="newItem"></input>
    <button @click="addItem">Add</button>
</template>
