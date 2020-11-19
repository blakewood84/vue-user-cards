<template>
    <div class="container">
        <h2>Username: {{ username }}</h2>
        <h3>Age: {{ age }}</h3>
    </div>
</template>
<script>
export default {
    props: {
        username: {
            type: String,
            required: true
        },
        age: {
            type: String,
            rquired: true
        }
    }
}
// ActiveUser should output a username (h2) and age (h3)
</script>
<style>
    .container {
        border:1px solid black;
        border-radius: 15px;
        padding:20px;
        margin:20px 0px;
        width:300px;
        display:flex;
        align-items:center;
        justify-content: center;
        flex-direction: column;
    }
</style>