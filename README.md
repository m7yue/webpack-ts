* node 环境

* mkdir webpack-ts

* cd webpack-ts

* npm init -y

* npm install typescript ts-loader --save-dev

* tsc --init
  * tsc 命令进行初始化  项目根目录多了一个tsconfig.json文件

* npm install webpack-cli webpack dev-server -D

* 创建一个build文件夹，里面创建webpack.config.js文件,配置相关代码

* npm install ts-loader -D
  * 解析ts文件转换成浏览器可以识别的文件

* npm install cross-env -D
  * 用于设置环境变量的,方便设置开发环境和生产环境

* npm install clean-webpack-plugin html-webpack-plugin -D
  * clean-webpack-plugin 能清理一些指定的文件夹
  * html-webpack-plugin 指定一个编译的模型

* package.json文件中写指定的命令
  ```json
    "scripts": {
      "start": "cross-env NODE_ENV=development webpack-dev-server --config ./build/webpack.config.js",
      "build": "cross-env NODE_ENV=production webpack --config ./build/webpack.config.js"
    },
  ```

* 创建文件
  * 在src的目录下，创建./src/index.ts
  * 在src的目录下，创建template文件夹
  * 在template文件夹下边创建index.html

* 启动本地服务器执行
  * npm start