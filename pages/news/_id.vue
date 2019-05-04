<template>
    <div style="border:1px solid #000">
        <h2>News-content</h2>
        <p>NEwsId:{{$route.params.id}}</p>
        <ul>
            <li><nuxt-link to="/">Home</nuxt-link></li>
        </ul>
    </div>
</template>
<script>
    export default{
        validate ({params}){
            return /^\d+$/.test(params.id);
        },
        data() {
            return {
                title:this.$route.params.title,
            }
        },
        head(){
            return {
                title:this.title,
                meta:[
                    {hid:'description',name:'news1',content:'This is news page'}
                ]
            }
        }
    }
</script>
