# React Hooks
#### 什么是Hooks
**官方介绍：** Hook 是 React 16.8 的新增特性。它可以让你在不编写 class 的情况下使用 state 以及其他的 React 特性。

**个人理解：** 函数式组件plus

#### Hooks 解决了什么问题
1. **类组件的this指向：** 函数式组件，没了类当然就解决了

2. **类组件太过沉重：** 之前类组件想写个小组件，需要写很多跟跟逻辑不相关的代码like this

**class版**

``` js
class Example extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      count: 0
    };
  }

  render() {
    return (
      <div>
        <p>You clicked {this.state.count} times</p>
        <button onClick={() => this.setState({ count: this.state.count + 1 })}>
          Click me
        </button>
      </div>
    );
  }
}
```

**hooks版**

``` js
import { useState } from 'react';

function Example() {
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>
        Click me
      </button>
    </div>
  );
}
```

3. **函数式组件的没有生命周期钩子：**react 本身也支持纯函数组件，但是，这种写法有重大限制，必须是纯函数，不能包含状态，也不支持生命周期方法，因此无法取代类。




