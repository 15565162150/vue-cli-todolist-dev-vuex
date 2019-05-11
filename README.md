# vue-cli-todolist-dev-vuex
Vue-cli-todolist是一个用vue-cli3工具初始化项目，相关的技术栈：Vue-cli3， Vue，VueRouter。
一.拆分组件的难点在于，组织结构上趋于分散，但数据处理上趋于集中，集中的数据便于管理或驱动页面视图。 组件是Vue开发当中最小的组成单元，以.vue扩展名结尾。
二.home.vue：
            1. main-view表示组件名称，如果是全局组件那名称是唯一的；
            2.:todos="filteredTodos"，冒号表示变量是动态的，如果不是冒号默认是String，todos表示子组件接受数据的变量名称，filteredTodos表示当前页面的变量名称；
二.Header.vue：
            1.home.vue中输入<header>....</header>，组件名称不能与HTML的原有标签名称重复，否则当普通的html标签解析；
三.Main.vue：
            1.:class
              对象语法 { active: isActive, 'text-danger': hasError }，通过Boolean值控制是否有值
              数组语法 [activeClass, errorClass]，通过变量合并显示 ；
            2.@dblclick，@click 绑定事件的缩写形式，完整的为：v-on:click="handle"；
            3.{{ item.title }} 基础变量显示，原始html需要v-html="rawHtml"指令；
            4.@keyup.enter.prevent 通过事件修饰符连写，达到处理冒泡，阻止自定义事件等等的目的
            5.computed -> set || get 一般计算属性默认都是getter，全选的处理需要主动的修改数据源；
            6.props接受数据，data初始化变量；
四.package.json：
            1.dependencies 上线依赖，npm i -S moduleName；
            2.devDependencies 开发依赖 npm i -D moduleName；
            
            
