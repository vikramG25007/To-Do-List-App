<script setup>
</script>

<template>
        <div id="parent">
            <div class="container">
                <div class="glassmorphism">
                <!-- Your login form goes here -->
                <h2>Login To Do</h2>
                <form>
                    <div class="input-wrapper">
                        <input type="text" placeholder="" required v-model="username">
                        <label :class="{ 'active': username }">Username</label>
                    </div>
                    <div class="input-wrapper">
                        <input type="password" placeholder="" required v-model="password">
                        <label :class="{ 'active': password }">Password</label>
                    </div>
                    <button type="submit">Login</button>
                </form>
               </div>
            </div>
        </div>
</template>


<style scoped>

@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,400;0,500;1,900&display=swap');

#parent{
    width: 100vw;
    height: 100vh;
    background-image:url('../assets/Designer.png')!important;
    background-size: cover;
    background-repeat: no-repeat;
    background-position: top;
}

h2{
  font-family: 'Poppins', sans-serif;
  font-weight: 200;
}
.container {
    height: 100%;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
}

.glassmorphism {
    display: flex;
    flex-direction: column;
    justify-content: center;
    width: 500px;
    height:400px;
    background: rgba(255, 255, 255, 0.2);
    backdrop-filter: blur(10px);
    border-radius: 20px;
    box-shadow: 0 8px 32px 0 rgba(31, 38, 135, 0.37);
    backdrop-filter: blur(20px);
    -webkit-backdrop-filter: blur(20px);
    border: 1px solid rgba(255, 255, 255, 0.18);
}

.glassmorphism input{
    width:70%!important;
}

.glassmorphism form {
    display: flex;
    flex-direction: column;
    align-items: center;
}

.glassmorphism h2 {
    text-align: center;
    color: #fff;
    margin-bottom:50px;
}

input{
   padding: 10px;
   margin-bottom:10px;
}

button {
    font-family: 'Poppins', sans-serif;
    width: 40%;
    border: none;
    border-radius: 25px;
    background-color: rgba(255, 255, 255, 0.2);
    backdrop-filter: blur(10px);
    color: #fff;
    outline: none;
    margin-bottom: 25px;
}

.glassmorphism button {
    cursor: pointer;
    transition: all .5s ease-in-out;
    font-family: 'Poppins', sans-serif;
    font-weight: bold;
    padding: 15px ;
}

.glassmorphism button:hover {
    background-color: rgb(255, 255, 255);
    backdrop-filter: blur(10px);
    color: black;
}

.input-wrapper {
    position: relative;
    margin-bottom: 15px;
    width:80%;
    display: flex;
    justify-content: center;
}

label{
    font-family: 'Poppins', sans-serif;
}

.input-wrapper input {
    width: 100%;
    padding: 15px;
    border: none;
    border-radius: 5px;
    /* background-color: rgba(255, 255, 255, 0.2);
    backdrop-filter: blur(10px); */
    color: #fff;
    border-radius: 15px;
    outline: none;
}

.input-wrapper label {
    position: absolute;
    top: 10px;
    left: 15px;
    font-size: 16px;
    color: rgb(0, 0, 0);
    transition: all 0.3s ease;
    pointer-events: none;
    margin-left: 45px;
}

.input-wrapper input:focus + label,
.input-wrapper input:not(:placeholder-shown) + label {
    top: -20px;
    font-size: 12px;
    color: #fff;
}


</style>
