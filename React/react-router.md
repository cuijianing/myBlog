### 区别

#### BrowserRouter

- `BrowserRouter` 使用 `HTML5 history API`, 保证`UI界面`和`URL`保存同步
采用这种方式需要后端或者`Nginx`配置通配路由, 比如在某个路径下重定向到模板首页 否则路由刷新页面时会404

- 传值方式: url传值, 路由参数传值, 以及state

- 不支持历史记录功能

#### HashRouter

- `HashRouter`使用 `URL`(即 `window.location.hash`) 的哈希部分来保持UI与URL同步的。哈希历史记录不支持`location.key`和`location.state` 用来支持旧版浏览器, 官方不建议使用

- 传值方式: url传值, 路由参数传值
---
### 属性

#### history
- **length**: number 浏览历史堆栈中的条目数

- **action**: string 路由跳转到当前页面执行的动作，分为 PUSH, REPLACE, POP

- **location**: object 当前访问地址信息组成的对象，具有如下属性：
    - pathname: string URL路径
    - search: string URL中的查询字符串
    - hash: string URL的 hash 片段
    - state: string 例如执行 push(path, state) 操作时，location 的 state 将被提供到堆栈信息里，state 只有在 browser 和 memory history 有效。
- **push**:(path, [state]) 在历史堆栈信息里加入一个新条目。
- **replace**:(path, [state]) 在历史堆栈信息里替换掉当前的条目
- **go**:(n) 将 history 堆栈中的指针向前移动 n。
- **goBack()**: 等同于 go(-1)
- **goForward()**: 等同于 go(1)
- **block(prompt)**: 阻止跳转


---
### 参考

[BrowserRouter](https://github.com/ReactTraining/react-router/blob/b77283cb75/packages/react-router-dom/docs/api/BrowserRouter.md)

[HashRouter](https://github.com/ReactTraining/react-router/blob/b77283cb75/packages/react-router-dom/docs/api/HashRouter.md)

[MemoryRouter](https://github.com/ReactTraining/react-router/blob/b77283cb75/packages/react-router-dom/docs/api/MemoryRouter.md)

[history](https://github.com/ReactTraining/history)