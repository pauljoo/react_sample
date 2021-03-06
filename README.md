## 目录结构

node_modules： 这里面包含了react项目中会用到的一些组件，install的时候下载下来的。  

public：里面包含了我们项目中的启动页面，react比较适合单页面项目应用开发，所以暂时只包含一个index.html，并且这也是react工程的入口页面。  

src：里面包含了一些我们自己使用的js文件，css文件，img文件等等。  

```
src/                 所有源代码存放的路径
  app.js             整个应用的入口
  views/             应用中某个页面的入口文件，一般为路由组件
    Home.js          例如，首页的入口就是Home.js
    Home.css         Home页面对应的样式
    HomeRedux.js     Home页面中所有与Redux相关的reducer、action creator的汇总，即components/Home/下所有*Redux.js的汇总
  components/        所有应用的组件
    Home/            例如，views/中一个名为Home的view，则在components/中就有一个名为Home的子文件夹
      Table.js       Home页面中的一个列表组件
      Table.css      列表组件对应的样式
      TableRedux.js  列表组件的reducer、action creator及action type，整合在一个文件中
      Modal.js
      Modal.css
      ModalRedux.js
    shared/          不归属于任何view的组件，如一些公共组件等
  containers/
    DevTools.js      配置DevTools
    Root.js          一般被app.js依赖，用于根据环境判断是否需要加载DevTools
  layouts/           布局相关的组件及样式，如菜单、侧边栏、header、footer等
  redux/             Redux store相关的配置
    reducers.js      整个应用中所有reducer的汇总
  routes/            路由相关的配置
  utils/             工具函数、常量等
  styles/            全局公共样式
  app.css            应用主样式表
```