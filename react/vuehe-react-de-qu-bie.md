## vue 和 react 的区别

#### vue

将标记放在HTML文件中是Vue应用程序的默认选项。与Angular类似，大括号用于数据绑定表达式，指令（特殊的HTML属性）用于向模板添加功能。

```js
<div id="app">
  <p>{{ message }}</p>
  <button v-on:click="reverseMessage">Reverse Message</button>
</div>

new Vue({
  el: '#app',
  data: {
    message: 'Hello Vue.js!
  },
  methods: {
    reverseMessage: function () {
      this.message = this.message.split('').reverse().join('');
    }
  }
});
```

#### React

整个组件更像一个ES6的类

```js
 class App extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      message: 'Hello React.js!'
    };
  }
  reverseMessage() {
    this.setState({ 
      message: this.state.message.split('').reverse().join('') 
    });
  }
  render() {
    return (
      <div>
        <p>{this.state.message}</p>
        <button onClick={() => this.reverseMessage()}>
          Reverse Message
        </button>
      </div>
    )
  }
}
ReactDOM.render(App, document.getElementById('app'));
```

## 

## 参考

[React还是Vue？](https://segmentfault.com/a/1190000009268926)



