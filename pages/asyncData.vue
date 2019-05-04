<template>
    <div>
        <p>姓名：{{info.name}}</p>
        <p>年龄：{{info.age}}</p>
    </div>
</template>
<script>
import axios from 'axios'
export default {
    data() {
        return {
            name:"Hello word!"
        }
    },
    //组件创建之前获得的数据，不能用this
    // asyncData() {
    //     return axios.get('https://api.myjson.com/bins/udkt0').then((res)=>{
    //         return {info:res.data}
    //     })
    // },
    async asyncData() {
        let {data} = await axios.get('https://api.myjson.com/bins/udkt0')
        return {info:data}
    },
}
</script>
