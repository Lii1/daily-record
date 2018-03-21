### 清除筛选框条件-问题

1. 清空后如何重新获取数据，为何会存在500错误；this.getData() 未定义。。。 
2. 不够仔细 只能说  问题其实很明显

### 记录未修改的地方

​	添加的代码：

```javascript
@keyup.enter='search'

<ClearAllBtn v-on:clearAllFilter='clearAllFilter'>
                    <button slot='queryBtn' type='button' class="common-btn imp" @click='search'>查询</button>
                </ClearAllBtn>

methods: {
            clearAllFilter() {
                Object.keys(this.query).forEach(key => {
                    if(key !== 'list_type') {
                       this.query[key] = '' 
                    }
                })
                Object.keys(this.lazyQuery).forEach(key => {
                    this.lazyQuery[key] = ''
                })
            }
        }
```

1. ~~erpClient.vue  使用了模板~~

2. 要重新修改样式

3. ~~收款列表 服务器出错. 因为没有合并代码~~

4. 有个bug(vue相关的) 

   a oh. 白做了

   重来一次：

   ```
   <ClearAllBtn @clearAllFilter='clearAllFilter' @keyupForSearch='search'>
                   <div>
                   </div>
               </ClearAllBtn>
               
   clearAllMixin

   export const clearAllMixin = {
       methods: {
           clearAllFilter() {
               Object.keys(this.query).forEach(key => {
                   if(key !== 'list_type') {
                       this.query[key] = '' 
                   }
               })
               Object.keys(this.lazyQuery).forEach(key => {
                   this.lazyQuery[key] = ''
               })
           }
       }
   }

   // 清空筛选条件
   Vue.component('ClearAllBtn', ClearAllBtn)

   // 清空筛选框筛选条件组件
   import ClearAllBtn from 'components/ClearAllFilters'
   ```

   待解决的问题：

   1. erp列表slot的问题；erprolelisttmpl.js
   2. ​

好玩的TYPORa

X^2^

<u>underline</u>

==highlight==



