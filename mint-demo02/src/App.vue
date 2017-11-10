<template>
    <div id="app">

        <!-- 按钮 -->
        <div class="my-btn-box">
          <mt-button type="default">default</mt-button>
          <mt-button type="primary" @click="open">加载数据</mt-button>
          <mt-button type="danger">danger</mt-button>
        </div>
    </div>
</template>

<script>
import { Indicator } from 'mint-ui';
export default {
    name: 'app',
    data () {
        return {
        }
    },
    methods:{
        open(){
            Indicator.open('加载中...');

            /*axios.get(xxx,{}).then(function(response){
                Indicator.close();
            }).catch()*/       //实际上这样写,请求数据成功后消失

            setTimeout(()=>{
                Indicator.close();
            },2000);
        }
    }
}
</script>

