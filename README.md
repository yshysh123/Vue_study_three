# Vue_兄弟组件传递bus
```
import Vue from 'vue';
export default new Vue();
```
//定义公共文件
·······································································································································································
```
import bus from 'components/public.js'   //引用相同文件
 methods: {
      addCart (event) {
        bus.$emit('caradd', event.target);
      }
    }
```
·····························································································································································
```
import bus from 'components/public.js'    //引用相同文件
created () {
      bus.$on('caradd', (res) => {
        console.log(res);
      });
 }
//B组件接收数据，控制台就能输出了
```
