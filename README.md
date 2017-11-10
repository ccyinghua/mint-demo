## mint-demo

> 基于vue.js的移动端组件库

- [mint-demo01 全部引入](https://github.com/ccyinghua/mint-demo/tree/master/mint-demo01)
- [mint-demo02 按需求引入](https://github.com/ccyinghua/mint-demo/tree/master/mint-demo02)

### Build Setup

```javascript
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report

```
### 构建项目

```javascript
#全部引入#：

vue init webpack-simple mint-demo

cnpm install

npm run dev

cnpm install mint-ui -D  //安装mint-ui

cnpm install style-loader -D
        -> webpack.config.js     配置
            {
                test: /\.css$/,
                loader: 'style-loader!css-loader'
             },

        -> webpack.config.js     字体图标配置
            {
                 test: /\.(eot|svg|ttf|woff|woff2)(\?\S*)?$/,
                 loader: 'file-loader'
            },
            
        
```

```javascript
#需求引入#： 以上全部引入配置 加上（+）

npm install babel-plugin-component -D   // 安装 babel-plugin-component

.babelrc文件修改

```

### mint-ui移动端ui库的使用
  
[http://mint-ui.github.io/#!/zh-cn](http://mint-ui.github.io/#!/zh-cn)

```javascript
1.安装 element-ui
    npm install mint-ui --save-dev

2.全部引入
    import Mint from 'mint-ui';
    import 'mint-ui/lib/style.css'
    Vue.use(Mint);

3.按需引入:借助 babel-plugin-component，安装 babel-plugin-component

    npm install babel-plugin-component -D

3.1将 .babelrc 文件新增配置
    "plugins": [["component", [
        {
          "libraryName": "mint-ui",
          "style": true
        }
      ]]]

3.2想用哪个组件就引用哪个组件，比如 Button 和 Cell  //main.js或者单独js然后用main.js引用即可

    import { Button, Cell } from 'mint-ui'

    Vue.component(Button.name, Button)
    Vue.component(Cell.name, Cell)
    /* 或写为
     * Vue.use(Button)
     * Vue.use(Cell)
     */

     
```
mint的简单练习： [https://github.com/itstrive/striveCode/tree/js/vue2.0-Mint-ui-demo 
](https://github.com/itstrive/striveCode/tree/js/vue2.0-Mint-ui-demo 
)








