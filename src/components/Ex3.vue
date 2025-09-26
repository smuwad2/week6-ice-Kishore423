<script>
    export default { 

        data(){
            return{
                loginoption:'username'

            }

        },
       // add code here

    }
</script>

<template>
    <h1>Please select your login option</h1>
    <!-- Add/modify code in the following to have a dropdown list 
        which lets the user to select either to login with username or email -->
    <select v-model="loginoption">
        <option value='username' selected>Username login</option>
        <option value="email">Email login</option>
    </select>
    
    <div v-if="loginoption==='username'" >
        <label>Username</label>
        <input placeholder="Enter your username">
    </div>
    <div v-else-if="loginoption === 'email'">
        <label>Email</label>
        <input placeholder="Enter your Email">
    </div>
</template>

