# 开始1234567890111

#



# 插槽
* 1. 组件标签使用时，如果子组件没有<slot>元素，那么，组件起始标签和结束标签之间的任何内容都会被抛弃。
* 2. 自 2.6.0 起有所更新。已废弃的使用 slot attribute 的语法在这里。
* 一个不带 name 的 <slot> 出口会带有隐含的名字“default”。
* 具名插槽
    <slot name="header"></slot>
    使用时，在一个 <template> 元素上使用 v-slot 指令即可，任何没有被包裹在带有 v-slot 的 <template> 中的内容都会被视为默认插槽的内容。

    v-slot 只能添加在 <template> 上 (只有一种例外情况)，这一点和已经废弃的 slot attribute 不同。


    缩写，v-slot: 替换为字符 #。例如 v-slot:header 可以被重写为 #header：   #后必须要带上参数，比如default



* 自 2.6.0 起有所更新。已废弃的使用 slot-scope attribute 的语法在这里。带有 slot attribute 的具名插槽也废弃


* 插槽prop
    绑定在 <slot> 元素上的 attribute 被称为插槽 prop。现在在父级作用域中，我们可以使用带值的 v-slot 来定义我们提供的插槽 prop 的名字

    <span>
    <slot v-bind:user="user">
        {{ user.lastName }}
    </slot>
    </span>


* 默认插槽的简化写法
    <current-user v-slot="slotProps">
    {{ slotProps.user.firstName }}
    </current-user>

    默认插槽的缩写语法不能和具名插槽混用，因为它会导致作用域不明确：
    当被提供的内容只有默认插槽时，组件的标签才可以被当作插槽的模板来使用。这样我们就可以把 v-slot 直接用在组件上

 * 渲染
    Vue 通过建立一个虚拟 DOM 来追踪自己要如何改变真实 DOM
    “虚拟节点 (virtual node)”，也常简写它为“VNode”。“虚拟 DOM”是我们对由 Vue 组件树建立起来的整个 VNode 树的称呼。

* 异步组件暂不看
动态组件，<component v-bind:is="currentTabComponent"></component>

* 过渡的样式，暂不看

* 通过全局方法 Vue.use() 使用插件。它需要在你调用 new Vue() 启动应用之前完成

* 过滤器 
    全局过滤器 
        Vue.filter  创建全局过滤器
    
    局部过滤器
        组件的选项中定义本地 filters:


        过滤器可以串联，{{ message | filterA | filterB }}

        生产环境用的，vue.min.js，减少了一些warning

# 杂项待整理
* 
* 