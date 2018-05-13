# 开发规约

## 项目结构
---


---

### 配置 src/config

### 页面 src/module
页面的模块化是分工的基础   

#### 入口页面 src/index
- index.html
- /css/index.css 通过index.css导入的方式进行模块化

#### 多页面 src/page

### 组件 component
组件的抽象化是复用的基础

#### 项目组件 src/component

### 公用库 src/common
### 公用组件 src/common/component

### 工具集 src/util

### 资源 src/asset
#### 模块化
- 大图 /image
    意味着要进行压缩处理，优化等
- 图标 /icon
    可以选择性变成base64引入
- 媒体 /media
- 字体 /font
- app使用的文档 /doc

### 本地库 src/lib

### 路由 src/router

### 全局状态机 src/store

### 异常 src/catch
#### error

#### empty

### 多线程 Service Worker /worker

## 测试
### [Jest](https://facebook.github.io/jest/)

## 编码约定

## 代码
### JSX

### JS

### CSS - [css-module](https://github.com/css-modules/css-modules)
- TODO: 预处理引入
> [如何在 React 中运用 CSS？](https://www.zhihu.com/question/30757566)
- 类名
- id

### es版本
- babel-preset
- .babelrc

### 代码格式化
- .editconfig

### 代码检查
- .eslintrc
> [react-native](https://www.npmjs.com/package/eslint-config-react-native)

- .eslintignore

### ignore文件
- .gitignore

## 文档化
### 文档要发挥的作用

### 文档种类
1. markdown [语法参考Stack OverFlow](https://stackoverflow.com/editing-help)
    - [readme](docs/template/readme.md)
    - [code](docs/template/code.md)
    - [changelog](docs/template/changelog.md)
    
2. 图
    - 流程图
    - 序列图
3. *表
    - 时间表
4. *脑图

### 文档维护时机

## 代码管理
### 1. 分支
|分支名|作用|说明|
|:-:|:-:|:-:|
|online|当前最新的线上发布包|tage必须为版本号|
|master|当前最新的线上源码|milestone的tag打在master上|
|release|所有版本源码的文件夹集合||
|dev|当前最新的开发源码||
|feature/yyyymmdd-name|当前开发版本的具体需求分支|从dev派生，不长久保留|
|demo|仅本项目用到库做的demo，比如react-native-pdf|一个模块的demo用一个文件夹，完全区分|

### 2. git提交
#### commit message
```bash
# 示例
# type(module): content
feat(login):  add hybrid support

# 1. type 改动类型
feat：新功能（feature）
fix：修补bug
docs：文档（documentation）
style： 格式（不影响代码运行的变动）
refactor：重构（既不是新增功能，也不是修改bug的代码变动）
test：增加测试
chore：构建过程或辅助工具的变动

# 2. module 模块
针对哪一个模块的改动

# 3. content 具体改动内容
```

### 3. 版本号
bspigai_1.0.0.180403_beta.apk
- app名称
- 主版本号：主线功能
- 子版本号：迭代需求
- 修订版本号：修订版本，如bugfix
- 日期版本号：180412
- 标识版本字段：alpha/beta/rc/release

## 部署与发布
- 构建 build.sh
- 部署线上 deploy.sh
- 部署测试 [deploy-test.sh](template/deploy-test.sh)

## [参考列表](reference-List.md)