# Dig into Apollo ![GitHub](https://img.shields.io/github/license/daohu527/Dig-into-Apollo.svg?style=popout)
![logo](img/logo.jpg)  

创建这个项目的初衷是为了在自动驾驶的学习过程中留下一些笔记，参考了不少网络上的资料和个人博客，有的时候真想拍案惊呼，为什么仅仅依靠网络和自学就能够做到如此优秀！也因此敦促自己不断学习和贡献优秀的笔记。  
> 子曰： 知之者不如好之者，好之者不如乐之者。  

👏️👏️👏️在这里特此感谢@[百度Apollo项目](https://github.com/ApolloAuto/apollo) @[3Blue1Brown](https://space.bilibili.com/88461692/) @[台大李宏毅](https://www.bilibili.com/video/av23593949/) @[iMorpheusAI](https://i.youku.com/i/UNTMxNDU3NjEwMA==?spm=a2hzp.8244740.0.0) @[阿Paul哥](https://paul.pub/about/)  


##  📒️ 目录
- [apollo简介](introduction)
    - [简介](introduction#introduction)
    - [目录结构](introduction#content)
    - [编译](introduction#compile)
- [Map](map)
    - [Map模块简介](map#introduction)
    - [Map目录结构](map#content)
    - [地图数据结构](map#map_data_struct)
        - [地图信息头](map#header)
        - [人行横道](map#crosswalk)
        - [路口](map#junction)
        - [车道](map#lane)
        - [停止信号](map#stop_sign)
        - [交通信号标志](map#signal)
        - [让行](map#yield)
        - [重叠区域](map#overlap)
        - [禁止停车](map#cleararea)
        - [道路信息](map#road)
        - [停车区域](map#parking)
        - [行人道路](map#sidewalk)
    - [opendriver地图解析](map#parse)
    - [高精度地图API](map#api)
    - [如何制作高精度地图](map#how)
        - [采集](map#collect)
        - [加工](map#process)
        - [转换](map#transform)
    - [Reference](#reference)
- [Localization](localization)
- [Perception](perception)
    - [CNN](perception/cnn)
        - [什么是CNN？](perception/cnn#what_is_cnn)
        - [CNN的原理](perception/cnn#cnn_principle)
            - [卷积层(Convolutional Layer)](perception/cnn#convolutional)
            - [池化层(Max Pooling Layer)](perception/cnn#max_pool)
            - [全连接层(Fully Connected Layer)](perception/cnn#fully_connect)
        - [如何构建CNN](perception/cnn#how_to)
        - [基本概念](perception/cnn#base_concept)
        - [引用](perception/cnn#reference)
    - [Caffe2](perception/caffe2)
        - [Caffe2环境准备](perception/caffe2#env)
        - [安装显卡驱动](perception/caffe2#drivers)
        - [安装CUDA](perception/caffe2#cuda)
            - [选择CUDA版本](perception/caffe2#cuda_version)
            - [安装CUDA](perception/caffe2#cuda_install)
            - [设置环境变量](perception/caffe2#cuda_env)
            - [检验安装](perception/caffe2#cuda_check)
        - [安装cuDNN](perception/caffe2#cudnn)
        - [安装Caffe2](perception/caffe2#caffe2)
        - [参考](perception/caffe2#reference)
    - [perception](perception)
- [Routing](routing)
    - [Routing模块简介](routing#introduction)
    - [基础知识](routing#base)
      - [Demo](routing#demo)
      - [地图](routing#map)
      - [最短距离](routing#shortest_path)
    - [Routing模块分析](routing#routing)
      - [创建Routing地图](routing#create_routing_map)
      - [Routing主流程](routing#routing_main)
    - [调试工具](routing#tools)
    - [问题](routing#question)
    - [OSM数据查找](routing#osm_find)
    - [Reference](routing#reference)
- [Planning](planning)
    - [Planning模块简介](planning#introduction)
      - [Planning输入输出](planning#planning_io)
      - [Planning整个流程](planning#planning_flow)
    - [Planning模块入口](planning#planning_entry)
      - [模块注册](planning#planning_register)
      - [模块初始化](planning#planning_init)
      - [模块运行](planning#planning_proc)
    - [OnLanePlanning](planning#onLanePlanning)
      - [初始化](planning#onLanePlanning_init)
      - [事件触发](planning#onLanePlanning_trigger)
    - [Planner](planning#planner)
      - [Planner注册场景](planning#planner_register)
      - [运行场景](planning#planner_plan)
    - [Scenario](planning#scenario)
      - [场景转换](planning#scenario_update)
      - [场景运行](planning#scenario_process)
    - [Task](planning#task)
      - [DP & QP](planning#dp_qp)
    - [Reference](planning#reference)
- [Control](control)
    - [Control模块简介](control#introduction)  
- [Canbus](canbus)
- [Simulation](simulation)
    - [为什么需要仿真](simulation#why_simulation)
    - [如何仿真](simulation#how_simulation)
        - [仿真软件](simulation#simulator)
        - [工作方式](simulation#simulator_work)
        - [工作原理](simulation#simulator_principle)
    - [如何使用](simulation#how_to)
        - [桥接器](simulation#adapter)
        - [制作地图](simulation#make_map)
        - [测试场景](simulation#test_case)
        - [功能多样化](simulation#features)
    - [参考](simulation#reference)
- [Cyber](cyber)
    - [How do you design cyber?](cyber#how)
    - [需求分析](cyber#requirements)
    - [系统设计](cyber#design)
      - [随意的假设](cyber#hypothesis)
      - [多节点](cyber#multinode)
      - [通信方式](cyber#communication)
      - [资源调度](cyber#schedule)
      - [软件复用](cyber#reuse)
      - [快速测试](cyber#test)
    - [其他](cyber#other)
      - [云平台](cyber#cloud)
    - [Reference](cyber#reference)
- [Performance](performance)
    - [线程调度](performance#schedule)
    - [Cgroups](performance#cgroups)
    - [CPU亲和性](performance#cpu)
    - [中断绑定](performance#interrupt)
    - [linux性能优化](performance#linux)
      - [Perf安装](performance#perf)
      - [火焰图](performance#flame_graph)
    - [Reference](performance#reference)
- [Transform](transform)
    - [Transform模块简介](transform#introduction)
    - [Transform(静态变换)](transform#static_transform)
    - [transform_broadcaster（广播）](transform#no_static_transform)
    - [Buffer（接收缓存）](transform#buffer)
        - [缓存接口](transform#buffer_interface)
        - [缓存实现](transform#buffer_class)
    - [总结](transform#summary)
    - [Reference](transform#reference)
- [Drivers](drivers)
- [Dreamview](dreamview)
- [Toolbox](toolbox)



> 各个模块的介绍都在对应的子目录中，主流程放在readme.md中，一些细节的函数和疑问放在todo.md中，需要了解主流程直接看readme.md，如果要深挖整个代码可以参考todo.md。

##  ☕️️ 鸣谢
* 欢迎对项目的贡献，如果觉得项目对你有帮助✌️️，欢迎star❤️！  

##  📌️ 参考
[apollo](https://github.com/ApolloAuto/apollo)  
[awesome-self-driving-cars](https://github.com/daohu527/awesome-self-driving-cars)  
