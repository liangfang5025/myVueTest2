<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>Essential Links</h2>
    <ul>
      <li>
        <a
          href="https://vuejs.org"
          target="_blank"
        >
          Core Docs
        </a>
      </li>
      <li>
        <a
          href="https://forum.vuejs.org"
          target="_blank"
        >
          Forum
        </a>
      </li>
      <li>
        <a
          href="https://chat.vuejs.org"
          target="_blank"
        >
          Community Chat
        </a>
      </li>
      <li>
        <a
          href="https://twitter.com/vuejs"
          target="_blank"
        >
          Twitter
        </a>
      </li>
      <br>
      <li>
        <a
          href="http://vuejs-templates.github.io/webpack/"
          target="_blank"
        >
          Docs for This Template
        </a>
      </li>
    </ul>
    <h2>Ecosystem</h2>
    <ul>
      <li>
        <a
          href="http://router.vuejs.org/"
          target="_blank"
        >
          vue-router
        </a>
      </li>
      <li>
        <a
          href="http://vuex.vuejs.org/"
          target="_blank"
        >
          vuex
        </a>
      </li>
      <li>
        <a
          href="http://vue-loader.vuejs.org/"
          target="_blank"
        >
          vue-loader
        </a>
      </li>
      <li>
        <a href="https://github.com/vuejs/awesome-vue" target="_blank">
          awesome-vue
        </a>
      </li>
    </ul>
    <!--v-bind:title="message"-->
    <div>
      <span v-bind:title="message">加载title</span>
    </div>
    <!--v-if="message"-->
    <div v-if="seen">if是否可见</div>
    <!-- v-for="i in array"(循环) -->
    <div>
      <ul>
        <li v-for= "todo in todos" :key="todo.id">{{todo.text}}</li>
      </ul>
    </div>
    <!--处理用户输入，为了让用户和我的应用进行交互，我们可以用  v-on 指令添加一个事件监听器，通过他调用在Vue实例中定义的方法-->
    <div>
      <p>{{ msg }}</p>
      <button >逆转消息</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your firstVue.js App',
      message: '页面加载与' + new Date().toLocaleDateString(),
      seen: true,
      todos: [
        {text: '学习js', id: '111'},
        {text: '学习vue', id: '222'},
        {text: '学习webpack', id: '333'}
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
