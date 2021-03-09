# request-api

环境配置文件,存放在 npm 私有库中

### 上传到使用私有库中

1. 需要先配置 `** npm` 私有源，具体配置方案，可查看前端文档  `**-npm`  的使用。

2. 使用 `nrm use push` 切换到 `push` 源。

3. 修改 package.json 配置中版本号 `version` ，每次发布的时候都要递增。


### 使用方法

  1. 安装前需要 `nrm use ` 切换到 `` 私服中下载源

  2. 在项目中 `npm install requestUrl` 安装模块
  
  3. 在需要地方如下引用
  
```
  // pc 端引用
  import { webApi } from "requestUrl"

  
    // 赋值
    baseUrl: {
      dev: '', // 测试环境
      pro: webApi().baseUrl
    },
    uploadUrl: {
      dev: "", // local 环境
      pro: webApi().uploadUrl
    }

````
### 返回的参数

 1. `webApi` 是 pc 端的方法，里面根据不同的域名去判断返回相应的请求地址,返回的参数如下
  
    `baseUrl` : 业务请求地址 

    `uploadUrl` : 上传接口请求地址
    