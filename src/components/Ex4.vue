<script>
    export default { 
        data() {
            return {
                // Add code here
                blueBoth : true,
                blueBox: 'blueBox',
                redBox:'redBox',
                id: 'demo1'

            }
        },
        methods: { 
   			// Add code here
            changeColor(){
                this.blueBoth = !this.blueBoth

            }
		}
    }
</script>

<template>
    
    <!-- Modify code here -->
    <div class="container">
        <div v-bind:id="id" class='m-2' v-bind:class="{'blueBox':blueBoth,'redBox':!blueBoth}">
            div ID : {{id}} 
        </div>

        
        <button type='Button' v-bind:class="{'btn btn-primary' : blueBoth, 'btn btn-danger':!blueBoth}" @click="changeColor()">Change Color</button>
    </div>

</template>

<style scoped>
    .redBox {
        background-color: red;
    }
    .blueBox {
        background-color: blue;
    }
    #demo1 {
        color: white;
    }
</style>
