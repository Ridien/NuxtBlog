<template>
 <section class="container">
    <h1>
        <div  class="home">
            <a href="/">Back To Index</a>
        </div>
        <p>Type in some user id</p>
        <input type="text" name="" id="userinput" v-model="userinput">
        <button @click = "onLoadUser">Search</button>
        
        
    </h1>
    <nuxt-child />
 </section>
</template>

<script>
    export default{
        data(){
            return{
                userinput: ''
            }
        },
        methods: {
            onLoadUser: function(){
                this.$router.push('/users/' + this.userinput)
            }
        },
        layout: 'users'
    }
</script>

<style>
    .home{
        width:100px;
        height: 100px;
        background-color: red


    }
</style>