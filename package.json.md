#### 本地开发配置自定义全局命令
1. 配置package.json的bin字段可以用来存放一个可执行的文件，如下配置所示
```
"bin": {
    "dps": "bin/dps-cli.js"
  },
```
2. 执行npm link。它将会把app这个字段复制到npm的全局模块安装文件夹node_modules内，并创建符号链接（symbolic link，软链接），也就是将 app 的路径加入环境变量 PATH

3. 在bin的主入口文件bin/dps-cli.js的最上方添加代码 #! /usr/bin/env node, 表明这是一个可执行的应用
