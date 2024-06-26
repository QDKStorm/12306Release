<div align="center">
  <p>
      <img width="75%" src="./theme_picture.png" alt="YOLO Vision banner"></a>
  </p>
</div>

## <div align="center"> China Railway Transfer Planning</div>

China Railway Transfer Planning是为了解决12306官方应用查询中转时查询结果不全、方案不优、响应速度慢等问题而制作的应用程序。它基于离线的数据，利用图论方法求解路径，并提供了按时间筛选、同城换乘、夜发昼达等定制功能。

本仓库是CRTP的Qt工程仓库，主要包含图形化相关的文件。此外，你还可以在[China-Railway-Transfer-Planning-Dev](https://github.com/QDKStorm/China-Railway-Transfer-Planning-Dev)仓库中看到这个项目开发时使用的一些文件。

项目会定期更新最新的离线数据，但不会提供数据的来源。

项目还在进步中，欢迎提出建议！

### 用法

#### 通过Release

在[Release](https://github.com/QDKStorm/China-Railway-Transfer-Planning/releases)中下载包含可执行文件的压缩包，解压到任意位置后，双击其中的`12306中转查询.exe`即可使用。注意该exe文件只能够在该路径下使用，将它移动到其他位置将不能正常启动。

#### 通过源码

本仓库是CRTP的Qt工程仓库，可以在`Qt 6.6.2`环境下正常运行。执行

```bash
git clone git@github.com:QDKStorm/China-Railway-Transfer-Planning-Dev.git
```

后，在QtCreator中打开本仓库的所有文件。你可以在QtCreator中运行它。

### 文件结构

- `BFS.cpp`和`BFS.h`：寻路算法的源码，也包含一些图形化相关操作
- `graph.txt`：即离线数据，包含了列车时刻表信息、同城车站信息
- `hello.pro`：Qt项目文件，~~叫hello的原因是创建项目时写了个Hello, world试了试手~~

- `in.txt`：已经废弃的离线数据，它目前没有任何用处
- `main.cpp`：控制窗口显示的代码
- `mainwindow.cpp`、`mainwindow.h`和`mainwindow.ui`：窗口显示相关代码，包括窗口中的元素和样式、信号与槽。

### 注意

- 由于列车时刻表每季度一换，所以你需要手动保证程序是最新的。使用旧版的程序或离线数据可能会导致错误的计算结果。
- 本项目不提供12306官网的爬虫程序
