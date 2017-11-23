#自定义指令
##简介
对于刚接触vue的新手来说，一般对于vue里的指令只会用，不太了解，这样会在后期的使用中遇到很多问题,所以我写了一些简单的自定义指令，方便了解

```javascript
        Vue.directive('myhtml',{
           bind:function (el,binding) {
              el.innerHTML=binding.value;
           }
        })
        
        var vm=new Vue({
            el:'#app',
            data:{
                msg:'<h1>大家好</h1>'
            },
        })
        
```
```html

<div id="app">
    <div v-myhtml="msg"></div>
</div>

```
上面就是一个简单的自定义指令了，可以实现v-html