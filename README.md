# es6
慕课网：ES6零基础教学 解析彩票项目

记录日期：2018年03月31日21:20:53

运行环境：
macOS 10.13.4 

nodejs 8.11.1 lts

gulp 3.9.1

================

1 安装 nodejs 8.11.1

2 安装淘宝 cnpm 

```
# https://npm.taobao.org/
$ npm install -g cnpm --registry=https://registry.npm.taobao.org
```

3 解决依赖问题：

```bash

cnpm i babel-core babel-loader babel-plugin-transform-decorators-legacy babel-polyfill babel-preset-env babel-preset-es2015 connect-livereload del gulp gulp-concat gulp-if gulp-live-server gulp-livereload gulp-plumber gulp-rename gulp-sequence gulp-uglify gulp-util jquery require-dir vinyl-named webpack webpack-stream yargs express serve-favicon morgan cookie-parser mockjs ejs connect-livereload --save-dev
```

修改 `server/app.js` , 注意代码位置不要错，否则不起作用。
```
app.use(express.static(path.join(__dirname, 'public')));

// 热更新的实现
app.use(require('connect-livereload')());

app.use('/', index);
```

4 在项目根目录运行一下

```
gulp --watch
```

5 打开浏览器访问： <localhost:3000>

出处：<https://github.com/dzfuture007/es6>

