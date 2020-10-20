<template>
 <div>
  <h1>citylist</h1>
 </div>
    
</template>
<script>
import Vue from 'vue';
import VueAxios from 'vue-axios';
import axios from 'axios'
Vue.use(VueAxios,axios)
export default {
    name:"citylist",
    data(){
        return{
            list:undefined
        }
    },
    mounted(){
        Vue.axios.get('https://indian-cities-api-nocbegfhqg.now.sh/cities')
        .then(resp =>{
            this.list=resp.data.data
            console.warn(resp.data.data)

        })
    }
    
}
</script>