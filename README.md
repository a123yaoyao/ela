# ela
介绍
vue element-ui Build Status license GitHub release donate GitHub stars


vue-element-admin 是一个后台前端解决方案，它基于 vue 和 element-ui实现。它使用了最新的前端技术栈，内置了 i18 国际化解决方案，动态路由，权限验证，提炼了典型的业务模型，提供了丰富的功能组件，它可以帮助你快速搭建企业级中后台产品原型。相信不管你的需求是什么，本项目都能帮助到你。

建议

本项目的定位是后台集成方案，不太适合当基础模板来进行二次开发。因为本项目集成了很多你可能用不到的功能，会造成不少的代码冗余。如果你的项目不关注这方面的问题，也可以直接基于它进行二次开发。

集成方案: vue-element-admin
基础模板: vue-admin-template
桌面终端: electron-vue-admin
Typescript 版: vue-typescript-admin-template (鸣谢: @Armour)

# 功能
- 登录 / 注销

- 权限验证
  - 页面权限
  - 指令权限
  - 权限配置
  - 二步登录

- 多环境发布
  - dev sit stage prod

- 全局功能
  - 国际化多语言
  - 多种动态换肤
  - 动态侧边栏（支持多级路由嵌套）
  - 动态面包屑
  - 快捷导航(标签页)
  - Svg Sprite 图标
  - 本地/后端 mock 数据
  - Screenfull全屏
  - 自适应收缩侧边栏

- 编辑器
  - 富文本
  - Markdown
  - JSON 等多格式

- Excel
  - 导出excel
  - 导入excel
  - 前端可视化excel
  - 导出zip

- 表格
  - 动态表格
  - 拖拽表格
  - 内联编辑

- 错误页面
  - 401
  - 404

- 組件
  - 头像上传
  - 返回顶部
  - 拖拽Dialog
  - 拖拽Select
  - 拖拽看板
  - 列表拖拽
  - SplitPane
  - Dropzone
  - Sticky
  - CountTo

- 综合实例
- 错误日志
- Dashboard
- 引导页
- ECharts 图表
- Clipboard(剪贴复制)
- Markdown2html

# 前序准备
你需要在本地安装 node 和 git。本项目技术栈基于 ES2015+、vue、vuex、vue-router 、vue-cli 、axios 和 element-ui，所有的请求数据都使用Mock.js进行模拟，提前了解和学习这些知识会对使用本项目有很大的帮助。

同时配套一个系列的教程文章，如何从零构建后一个完整的管理后台项目，建议大家先看完这些文章再来实践本项目。

手摸手，带你用 vue 撸后台 系列一(基础篇)
手摸手，带你用 vue 撸后台 系列二(登录权限篇)
手摸手，带你用 vue 撸后台 系列三 (实战篇)
手摸手，带你用 vue 撸后台 系列四(vueAdmin 一个极简的后台基础模板)
手摸手，带你用 vue 撸后台 系列五(v4.0 新版本)
手摸手，带你封装一个 vue component
手摸手，带你优雅的使用 icon
手摸手，带你用合理的姿势使用 webpack4（上）
手摸手，带你用合理的姿势使用 webpack4（下）
本项目不支持低版本浏览器(如 ie)，有需求请自行添加 polyfill 详情

# 目录结构
本项目已经为你生成了一个完整的开发框架，提供了涵盖中后台开发的各类功能和坑位，下面是整个项目的目录结构。

├── build                      # 构建相关
├── mock                       # 项目mock 模拟数据
├── plop-templates             # 基本模板
├── public                     # 静态资源
│   │── favicon.ico            # favicon图标
│   └── index.html             # html模板
├── src                        # 源代码
│   ├── api                    # 所有请求
│   ├── assets                 # 主题 字体等静态资源
│   ├── components             # 全局公用组件
│   ├── directive              # 全局指令
│   ├── filters                # 全局 filter
│   ├── icons                  # 项目所有 svg icons
│   ├── lang                   # 国际化 language
│   ├── layout                 # 全局 layout
│   ├── router                 # 路由
│   ├── store                  # 全局 store管理
│   ├── styles                 # 全局样式
│   ├── utils                  # 全局公用方法
│   ├── vendor                 # 公用vendor
│   ├── views                  # views 所有页面
│   ├── App.vue                # 入口页面
│   ├── main.js                # 入口文件 加载组件 初始化等
│   └── permission.js          # 权限管理
├── tests                      # 测试
├── .env.xxx                   # 环境变量配置
├── .eslintrc.js               # eslint 配置项
├── .babelrc                   # babel-loader 配置
├── .travis.yml                # 自动化CI配置
├── vue.config.js              # vue-cli 配置
├── postcss.config.js          # postcss 配置
└── package.json               # package.json
# 安装
# 克隆项目
git clone https://github.com/PanJiaChen/vue-element-admin.git

# 进入项目目录
cd vue-element-admin

# 安装依赖
npm install

# 建议不要用 cnpm 安装 会有各种诡异的bug 可以通过如下操作解决 npm 下载速度慢的问题
npm install --registry=https://registry.npm.taobao.org

# 本地开发 启动项目
npm run dev

TIP

强烈建议不要用直接使用 cnpm 安装，会有各种诡异的 bug，可以通过重新指定 registry 来解决 npm 安装速度慢的问题。若还是不行，可使用 yarn 替代 npm。

Windows 用户若安装不成功，很大概率是node-sass安装失败，解决方案。

另外因为 node-sass 是依赖 python环境的，如果你之前没有安装和配置过的话，需要自行查看一下相关安装教程。


启动完成后会自动打开浏览器访问 http://localhost:9527， 你看到下面的页面就代表操作成功了。



接下来你可以修改代码进行业务开发了，本项目内建了典型业务模板、常用业务组件、模拟数据、HMR 实时预览、状态管理、国际化、全局路由等等各种实用的功能来辅助开发，你可以继续阅读和探索左侧的其它文档。


建议

你可以把 vue-element-admin当做工具箱或者集成方案仓库，在 vue-admin-template 的基础上进行二次开发，想要什么功能或者组件就去 vue-element-admin 那里复制过来。

# Contribution
本文档项目地址 vue-element-admin-site 基于 vuepress开发。

有任何修改和建议都可以该项目 pr 和 issue

vue-element-admin 还在持续迭代中，逐步沉淀和总结出更多功能和相应的实现代码，总结中后台产品模板/组件/业务场景的最佳实践。本项目也十分期待你的参与和反馈。

# 捐赠
如果你觉得这个项目帮助到了你，你可以帮作者买一杯果汁表示鼓励 ❤️ Donate

# Browsers Support
Modern browsers and Internet Explorer 10+.

IE / Edge
IE / Edge	Firefox
Firefox	Chrome
Chrome	Safari
Safari
IE10, IE11, Edge	last 2 versions	last 2 versions	last 2 versions
# 其它
群主 圈子 群主会经常分享一些技术相关的东西，或者加入 qq 群 或者关注 微博。

# Vue 生态圈
首先了解这些 vue 生态圈的东西，会对你上手本项目有很大的帮助。

Vue Router 是 vue 官方的路由。它能快速的帮助你构建一个单页面或者多页面的项目。

Vuex 是一个专为 Vue.js 应用程序开发的状态管理模式。它采用集中式存储管理应用的所有组件的状态，并以相应的规则保证状态以一种可预测的方式发生变化。它能解决你很多全局状态或者组件之间通信的问题。

Vue Loader 是为 vue 文件定制的一个 webpack 的 loader，它允许你以一种名为单文件组件 (SFCs)的格式撰写 Vue 组件。它能在开发过程中使用热重载来保持状态，为每个组件模拟出 scoped CSS 等等功能。不过大部分情况下你不需要对它直接进行配置，脚手架都帮你封装好了。

Vue Test Utils 是官方提供的一个单元测试工具。它能让你更方便的写单元测试。

Vue Dev-Tools Vue 在浏览器下的调试工具。写 vue 必备的一个浏览器插件，能大大的提高你调试的效率。

Vue CLI 是官方提供的一个 vue 项目脚手架，本项目也是基于它进行构建的。它帮你分装了大量的 webpack、babel 等其它配置，让你能花更少的精力在搭建环境上，从而能更专注于页面代码的编写。不过所有的脚手架都是针对大部分情况的，所以一些特殊的需求还是需要自己进行配置。建议先阅读一遍它的文档，对一些配置有一些基本的了解。

Vetur 是 VS Code 的插件. 如果你使用 VS Code 来写 vue 的话，这个插件是必不可少的。
