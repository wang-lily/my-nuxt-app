<template>
    <div>
        <h2>News Index page</h2>
        <p>NEwsId:{{$route.params.id}}</p>
        <ul>
            <li><nuxt-link to="/">Home</nuxt-link></li>
            <li><nuxt-link :to="{name:'news-id',params:{id:123,title:'news-title'}}">news-1</nuxt-link></li>
            <li><nuxt-link to="/news/edfd">news-2</nuxt-link></li>
        </ul>
    </div>
</template>
<script>
    export default{
        transition:'test'
    }
</script>
