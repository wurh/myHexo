title: 日记博客 终于从windows 上 转战到 mac 上
---
第一次开始博客编写，工作五年的老鸟了...
## 熟悉环境
``各种环境迁移， 需要配置各种环境变量， 如java,maven,node... 熟悉各种命令，用最快速度适应开发``

### 遇到的坑...

`` 运行 bash uae-pack.sh 时候一直报 maven compiler plugin 错误，后来发现 需要maven配置制定本地jdk目录地址``
`` git clone Funtime 工程， 执行 grunt 的时候又发现各种奇葩问题， 结果发现是代码问题 ``
`` 不得不说  mac os 好牛B ... ``

### 配置博客

`` 晚上配置博客时候，又遇到问题，安装 hexo 时候一直报 ``

```bash
    gyp WARN EACCES user “root” does not have permission to access the dev dir “/Users/xiangwenwen/.node-gyp/0.10.33”
```

`` 幸好有苏千的神贴，找到解决方案 ``

```bash
    npm i fsevents --registry=http://registry.npm.taobao.org --disturl=http://npm.taobao.org/mirrors/node --loglevel=http
```

### 总结
`` 第一天来说 虽然遇到的问题比较多，但是总算解决了，终于可与愉快的撸码了，收获甚多！！ 嘿嘿！ ``

