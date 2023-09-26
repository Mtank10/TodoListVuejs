<template>
   <h1>Todo List</h1>
   <div id="testing">
   <form @submit.prevent="addItem">
    <input type="text" v-model="newItem" placeholder="Add a new item"/>
    <button type="submit">Add</button>
   </form>
   <ul>
    <li v-for="(item,index) in item" :key="index">
    <span>{{ item }}</span>
    
    </li>
   </ul>
</div>
</template>

<script>
export default {
    name:"ClassAndStyle.vue",
    data:function(){
        return{
            newItem: "",
           item: [],
        }
    },
    method:{
        addItem(){
            if(this.newItem.trim()!==""){
                this.item.push(this.newItem);
            }
            this.newItem = ""
        }
    }
}
</script>
<style>
#testing li{
    border: 1px solid;
    padding: 5px;
}
</style>