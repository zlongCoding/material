# free-cli


init free cli 


### 发布npm流程
#### 本地文件创建
##### 1. 创建package.json
```
npm init
```
##### 2. 在package.json加入bin指令
```
  "bin": {
    "free": "lib/bin.js"
  }
```
#### 3. 在bin指令指定的目录创建脚本文件
lib/bin.js

```
#!/usr/bin/env node

console.log("初始化项目")
```

#### 发布

##### 重置npm镜像
```
npm config set registry http://registry.npmjs.org/
```
##### 登录
```
npm login
```
##### 发布公网

> 如果需要依赖于包发布

默认情况是npm 发布的都是一个独立的包，如果想依赖于整个包发布例如`@free-design`以后我所有的项目都在此包下面那么需要[创建包名](https://www.npmjs.com/org/create)





```
npm publish --access public
```
## 安装 和 更新
```
npm install @free-design/free-cli -g

npm install @free-design/free-cli@latest -g
```
## 使用
```
free 1
```