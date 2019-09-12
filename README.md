# AdonisJs官方网站中文版

假设运行的服务器是Linux或者Mac系统，并且已经安装配置好Node和Npm

- Node.js >= 8.0.0
- Npm >= 3.0.0

## 安装

安装AdonisJs Cli

```
npm i -g @adonisjs/cli
```

克隆项目

```
git clone https://github.com/guoshuohui/adonisjs.com.cn.git
cd adonisjs.com.cn
```

文档作为git子模块引用

```
git submodule init
git submodule update --remote
```

安装依赖

```
npm install
```

创建环境配置文件和密钥

```
cp .env.example .env
adonis key:generate
```

## 编译样式 & 脚本

```
npm run build
```

调试阶段可以设置保存文件立即编译

```
npm run build -- -w
```

## 编译文档

分别执行以下命令编译对应版本文档

```
adonis compile:docs --forVersion 3.2
adonis compile:docs --forVersion 4.0
adonis compile:docs --forVersion 4.1
```

调试阶段可以设置保存文件立即编译

```
adonis compile:docs --forVersion 4.1 --watch
```

## 启动服务

本地调试时可直接开启cli服务

```
adonis serve --dev
```

服务器部署推荐 [PM2](https://pm2.keymetrics.io/)，开启服务常驻

```
pm2 start server.js
```

## 注意

改版本只同步官方库的develop分支，与官网adonisjs.com内容一致，同时修复和调整了以下问题：

- 文档版本切换跳转链接错误
- css编译后无法压缩
- package.json依赖升级
- 文档子模块仓库直接集成3.2、4.0、4.1版本的内容，无需频繁切换修改和编译
