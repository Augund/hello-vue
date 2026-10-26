<template>
    <div class="person">
        <h1>姓名：{{ name }}</h1>
        <h1>年龄：{{ age }}</h1>
        <button @click="changeName">修改名字</button>
        <button @click="changeAge">修改年龄</button>
        <button @click="showTel">查看联系方式</button>
    </div>
</template>

<script lang="ts">
import { ref } from 'vue'

    export default{
        name:'Person',
        setup() {
            let name="joe"
            let age=20
            let tel="13022222222"

            function changeName(){
                name="zhang-san"
            }
            function changeAge(){
                age+=1
            }
            function showTel(){
                alert(tel)
            }

            return{name,age,tel,changeName,changeAge,showTel}
        }
    }
</script>

<style scope>
    .person{
        background-color: #f0f0f0;
        box-shadow: 0 0 10px;
        border-radius: 10px;
        padding: 20px;
    }
    button{
        margin: 10px;
    }
</style>