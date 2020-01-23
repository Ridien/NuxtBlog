<template>
    <section class= "container">
        <h1>
            This is some bloke, his id is: {{ $route.params.id }}
        </h1>
        <hr>
        <nuxt-link to = "/users">Back to users page</nuxt-link>
    </section>

</template>

<script>
export default {
    validate(data){
        return /^\d+$/.test(data.params.id)
    },
        layout: 'users'
}
</script>