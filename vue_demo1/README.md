## 语法
`v-bind:title="message"` 该指令的意思是：“将这个元素节点的 title 特性和 Vue 实例的 message 属性保持一致”   <br/>
`v-bind` 缩写 `:`  <br/>
`v-if="seen"` 可以在 Vue 插入/更新/移除元素时自动应用过渡效果  <br/>
`v-for="todo in todos"` 可以绑定数组的数据来渲染一个项目列表  <br/>
`v-on:click="reverseMessage"` 添加一个事件监听器  <br/>
`v-on:submit.prevent="onSubmit"` 对于触发的事件调用 event.preventDefault()  <br/>
`v-on` 缩写 `@`  <br/>
`v-model="message"` 它能轻松实现表单输入和应用状态之间的双向绑定  <br/>

## 组件
```
// 组件写法
Vue.component('todo-item', {
  props: ['todo'],
  template: '<li>{{ todo.text }}</li>'
})

var app7 = new Vue({
  el: '#app-7',
  data: {
    groceryList: [
      { id: 0, text: '蔬菜' },
      { id: 1, text: '奶酪' },
      { id: 2, text: '随便其它什么人吃的东西' }
    ]
  }
})
```
```
// 组件使用
<div id="app-7">
  <ol>
    <!--
      现在我们为每个 todo-item 提供 todo 对象
      todo 对象是变量，即其内容可以是动态的。
      我们也需要为每个组件提供一个“key”
    -->
    <todo-item
      v-for="item in groceryList"
      v-bind:todo="item"
      v-bind:key="item.id">
    </todo-item>
  </ol>
</div>
```
