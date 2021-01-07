# 入口(entry)

### 概念
`入口起点(entry point)`指示webpack应该使用哪个模块，来作为构建其内部`依赖图`的开始。进入入口起点后，webpack会找出有哪些模块和库是入口起点（直接和间接）依赖的。

### 用法
`entry: string | [] | {}`
- 单入口
- 多入口
---
#### 单入口
``` js
// webpack.config.js
module.exports = {
  entry: './path/to/my/entry/file.js'
};
```
---
#### 多入口
优点：可以减小打包细粒度, 将第三方库单独打包出来,利用浏览器缓存减少开销
``` js
// webpack.config.js
module.exports = {
  entry: {
    app: './path/to/my/entry/file.js',
    main: './path'
  }
};
```

``` js
// webpack.config.js
module.exports = {
    entry: ['./path/to/my/entry/file.js','./path']
};
```