Xw CLI是专为平时开发搭建的前端项目模板生成工具！


### 安装

``` 
    npm install -g xw-cli
```

### 使用

```
    xw create project-name       //走通用模板模式
    xw create project-name -s    //走高可配置模式
```
说明：
为适应现项目需求，特提供一个适应当前需求的快速版本，快速版本只需要执行xw create project-nam，再选择是否需要开启HTML模块化,雪碧图合并，px转rem功能就可下载适应当前开发的通用模板，该模板支持less用于CSS模块化,(AMD)require.js用于JS模块化开发，html(@include)模块化，name.ext?v=hash文件版本管理，px转rem,雪碧图生成功能；
同时也提供一个高度可定制化版本，执行xw create project-name -s,再按控制台选项选择需要的功能即可生成定制化模板，项目支持css模块化less/sass,js模块化AMD(require.js)/(commonjs)webpack/es6 module,html(@include)模块化，name.ext?v=hash文件版本管理，px转rem,雪碧图生成功能,版本管理name.ext?v=hash/name.hash.ext切换。

### 例如

```
    xw create project-name [-s]
```
上面的命令会在当前目录下新建一个名为project-name的项目，用户通过选择不同选项，命令会自动从GITHUB下载指定的模板文件,当带有-s时，会有如下选项，如不带-s，则只有如下可选项。

通用模板生成选项如下(xw create project-name)

    ? 请选择你需要集成的功能
        html模块化
        集成px转rem功能
        集成雪碧图合并功能


高可配置模板生成选项如下(xw create project-name -s)

    ? 选择模块化开发方式
    > 使用(AMD)requirejs管理
    > 使用(Commonjs)webpack管理
    > 使用es6 module

    ? 选择CSS预处理
    > 使用less管理css
    > 使用sass管理css

    ? 请选择你需要集成的功能
        html模块化
        集成px转rem功能
        集成雪碧图合并功能

    ? 选择文件版本管理方式
    > example.js?v=hash码，加search值版本管理方式
    > example.hash.js码，修改文件名的版本管理方式

模块项目运行步骤：

```
    cd project-name
    npm install         //安装模块
    npm run static      //走静态开发流程，通用模板才有
    npm run dev         //走开发流程，通用模板下是混合开发
    npm run build      //走发布流程
```
