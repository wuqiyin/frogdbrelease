[中文](./README.zh.md) | [English](./README.md)

FrogDB 是一款现代化桌面 SQL 查询客户端。

目前市场上已有多款 SQL 查询客户端，为何要重新研发一款？核心原因在于，现有 SQL 查询客户端普遍存在诸多痛点，影响使用体验与工作效率：

1. 工作空间缺乏隔离机制，导致表搜索、SQL 控制台中的脚本无法精准对应目标数据库，使用过程混乱无序；

2. 表查找操作繁琐，效率低下；

3. 当表字段数量较多时，无法快速定位目标列，需左右拖动查找，操作繁琐费力；

4. 不支持折线图、柱状图等可视化图表，难以满足数据分析需求；

5. 无法对列数据进行快速 JSON 格式化、URL Decode 解码等便捷操作；

6. 不支持快速隐藏表列，冗余字段影响数据查看；

7. 不支持 SQL 控制台自定义代码片段，重复编写常用脚本耗时费力。

针对以上痛点，FrogDB 均给出了高效、便捷的解决方案。

![logo](https://github.com/user-attachments/assets/eb1acca7-6a0c-466d-898e-a0f94d70a145)

## 产品概述

FrogDB 专为每日需处理多个数据库的开发人员、数据分析师及 DBA 量身打造。

它打破了 SQL 仅作为孤立查询窗口的传统模式，提供面向项目的工作空间，支持可重用的连接配置、标签页式执行上下文与快速数据导航功能。

我们的目标十分明确：在保障操作可控性与安全性的前提下，最大程度减少日常数据库操作的繁琐流程，提升工作效率。

![demo](https://github.com/user-attachments/assets/b1da0ef0-16a2-43bd-8c57-b076888cf2d0)

## 功能特性

### 数据库级别的工作空间

支持同时打开多个数据库，每个数据库的工作空间相互独立隔离，避免操作混乱。

![image](https://github.com/user-attachments/assets/dcdc46d7-edf1-46b0-8b2b-8026529d5be6)

进入数据库工作空间后，双击 Shift 快捷键，或点击右上角的搜索按钮，即可快速搜索该数据库内的所有表。

![image](https://github.com/user-attachments/assets/0b452be6-731e-470f-ad8d-532f7ac16894)

打开表后，按下快捷键 Command+O（Windows 系统为 Ctrl+F12），可快速跳转到目标表列。该快捷键与 JetBrains IDEA 保持一致，无需额外学习，零使用成本。

![image](https://github.com/user-attachments/assets/dd38dfed-3564-4e14-9a8c-00583c40c81f)

### 记住查询历史

在 WHERE 条件编辑框中，可直接选择历史查询记录，无需重复输入，便捷高效。

![image](https://github.com/user-attachments/assets/b0e27f01-8142-4a7d-acf2-b103b74f975d)

### 快速查看 DDL

点击右上角的「View DDL」按钮，即可快速查看当前表的 DDL 语句，无需手动编写查询。

![image](https://github.com/user-attachments/assets/ffd29311-bc14-46ca-bf95-05d9a7338c2f)

### 查看行数据

双击行序号，即可查看当前行的完整数据，无需切换视图。

![image](https://github.com/user-attachments/assets/a3f31706-79a2-474d-82ac-bf6f206cbd11)

### 查看单元格数据

双击单元格，可快速查看单元格详情，同时支持数据格式化功能，适配 JSON、URL 等多种数据格式。

![image](https://github.com/user-attachments/assets/1684f572-a5a1-4e9c-aa8d-36482277675c)

### 快速生成 SQL 语句

「Copy as IN Query」功能可快速生成 IN 条件语句，方便批量查询目标单元格值，示例如下：

```sql

IN ('luanqibazao')

```

「Copy as Update」功能可精准生成单个字段的更新语句，区别于其他 SQL 工具默认生成全字段更新语句的弊端，无需手动修改，大幅提升效率，示例如下：

```sql

UPDATE `uto_config` SET `type` = 'luanqibazao' WHERE `id` = 13;

```

![image](https://github.com/user-attachments/assets/e3b9811c-0502-40a5-8b7a-2a202653da8b)

若需生成整行记录的 INSERT、UPDATE 及 DELETE 语句，右键点击行序号并选择复制即可，示例如下：

![image](https://github.com/user-attachments/assets/004f2758-451e-41c7-b28a-5930f4d38ff6)

生成的 SQL 语句如下：

```sql

INSERT INTO `uto_config` (`cfg`, `created_at`, `id`, `type`, `updated_at`) VALUES (NULL, '2025-06-18 16:30:39', 13, 'luanqibazao', '2025-06-18 16:30:39');

UPDATE `uto_config` SET `cfg` = NULL, `created_at` = '2025-06-18 16:30:39', `id` = 13, `type` = 'luanqibazao', `updated_at` = '2025-06-18 16:30:39' WHERE `id` = 13;

DELETE FROM `uto_config` WHERE `id` = 13;

```

### 快速隐藏字段

支持快速隐藏冗余表字段，聚焦核心数据，提升查看效率。

![image](https://github.com/user-attachments/assets/adad0f3c-54d5-40eb-89a7-6322d5822b26)

### 快速搜索结果

支持对查询结果进行快速筛选，精准定位目标数据，无需重新执行查询。

![image](https://github.com/user-attachments/assets/ea97e6ca-cd43-47ee-bf18-d4c18fd5381a)

### 支持脚本

支持脚本保存功能，常用脚本可随时调用，避免重复编写。

![image](https://github.com/user-attachments/assets/7d21b944-e551-41a4-9203-ab15b8277bdd)

支持添加自定义代码片段，常用 SQL 片段可快速插入，提升编写效率。

![image](https://github.com/user-attachments/assets/b211d7e3-fc5f-4d32-9a71-3b8fdfb3926f)

### 支持图表

内置图表功能，支持折线图、柱状图等多种可视化形式，助力高效数据分析。

![image](https://github.com/user-attachments/assets/6ad790cb-1fa3-45b0-830e-4966c962d875)

### 其他

FrogDB 还包含诸多人性化功能，等待您探索发现：

- 多连接工作区，支持持久化连接配置文件，无需重复配置；

- 支持可选 SSH 隧道配置，实现安全的远程数据库访问；

- 只读保护模式，可拦截删除、修改等高危操作，保障数据安全；

- 基于 Monaco 的 SQL 编辑器，提供熟悉、高效的编码体验；

- 便捷的数据库与表探索功能，搭配结果面板与行级详情视图；

- 支持脚本与查询工作流，提供标签页式项目上下文管理；

- 丰富的可视化 UX 增强功能，如搜索面板、过滤工具、快速导航对话框等；

- 更多实用功能，持续迭代更新中。

## 核心优势

- 以集成式工作区优化日常 SQL 工作流，替代分散工具，提升协作与操作效率；

- 内置只读控制功能，为敏感数据库环境提供更可靠的操作安全保障；

- 一站式管理数据库连接、脚本与查询结果，减少上下文切换成本；

- 跨平台适配，支持混合操作系统团队协同使用。

## 典型使用场景

- 通过安全的只读查询会话，排查生产环境数据库问题，避免误操作；

- 跨多个数据库架构，开发并验证 SQL 脚本，确保兼容性；

- 快速探索不熟悉的数据库结构，通过表/数据快速检查，提升认知效率；

- 在可重用工作区中，管理周期性数据分析与临时查询任务，提升复用率。

## 产品定位

FrogDB 定位为一款以生产力为核心的 MySQL 桌面客户端：兼具强大功能与轻量体验，支持高级 SQL 工作流，适配日常高频使用场景，始终秉持安全、高效的执行理念，为数据库相关从业者提供更优质的操作体验。
