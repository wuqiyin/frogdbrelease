# FrogDB

[中文](./README.zh.md) | [English](./README.md)

FrogDB 是一个现代化桌面 SQL 查询客户端。

现在市场已经有很多sql查询的客户端了，为什么要重新开发一个呢？主要是因为现在市场上的sql 查询客户端有很多痛点：

1. 工作空间没有隔离，导致表搜索，或者 sql 控制台里的脚本，不能准确的针对某个数据库，使用起来很混乱
2. 表查找不方便
3. 表字段多的时候，不能快速定位到表的列，需要左右拖动寻找列，很费劲
4. 不支持折线图、柱状图等，这些对数据分析很重要
5. 不能支持对列进行快速的 json 格式化，url decode 解码等
6. 不支持快速的隐藏列
7. 不支持sql console 的自定义代码片段等

这些问题，frogdb 都较好的解决了。

![logo](https://github.com/user-attachments/assets/eb1acca7-6a0c-466d-898e-a0f94d70a145)


## 产品概述

FrogDB 专为每天处理多个数据库的开发人员、分析师和 DBA 设计。
不再将 SQL 视为孤立的查询窗口，FrogDB 提供了一个面向项目的工作区，支持可重用的连接配置、标签页式的执行上下文和快速数据导航。
目标很简单：减少日常数据库操作的摩擦，同时保持控制力和安全性。

![demo](https://github.com/user-attachments/assets/b1da0ef0-16a2-43bd-8c57-b076888cf2d0)

## 功能特性

### 数据库级别的的工作空间

支持打开多个数据库，每个数据库的工作空间是隔离的

<img width="1640" height="785" alt="image" src="https://github.com/user-attachments/assets/245aeae6-a8c4-44c3-aafe-08d2e77a7b98" />

进入数据库工作空间后，快捷键快速按两下 shift 键，或者点击右上角的 search 的按钮，可以快速搜索该数据库里的表

<img width="1639" height="784" alt="image" src="https://github.com/user-attachments/assets/0b452be6-731e-470f-ad8d-532f7ac16894" />

打开表的情况下，快捷键 command+o（windows 是 ctrl+f12）可以快速跳转到表的列，这个快捷键和 jetbrain 的 idea 的快捷键是一样的，没有使用成本

<img width="1634" height="786" alt="image" src="https://github.com/user-attachments/assets/dd38dfed-3564-4e14-9a8c-00583c40c81f" />





- 多连接工作区，支持持久化的连接配置文件
- 通过可选的 SSH 隧道配置实现安全的远程访问
- 只读保护模式，可拦截有风险的修改语句
- 基于 Monaco 的 SQL 编辑器，提供熟悉且高效的编码体验
- 数据库和表探索，配备结果面板和行级详情视图
- 支持脚本和查询工作流，提供标签页式项目上下文
- 可视化 UX 增强，如搜索面板、过滤工具和快速导航对话框

## 核心优势

- 通过集成式工作区实现更快的日常 SQL 工作流，而非使用分散的工具
- 通过内置的只读控制为敏感环境提供更好的操作安全性
- 在一个 UI 中管理连接、脚本和结果，降低上下文切换成本
- 跨平台交付模式，支持运行混合操作系统的团队

## 典型使用场景

- 使用安全的只读查询会话调查生产环境问题
- 跨多个架构开发和验证 SQL 脚本
- 通过快速表/数据检查探索不熟悉的数据库结构
- 在一个可重用的工作区中管理周期性分析和临时查询任务


## 产品定位

FrogDB 定位为以生产力为核心的 MySQL 桌面客户端：
功能强大，支持高级 SQL 工作流；轻量级，适合日常使用；倾向于安全、高效的执行方式。

