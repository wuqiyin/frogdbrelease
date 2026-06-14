# FrogDB

[中文](./README.zh.md) | [English](./README.md)

FrogDB is a modern desktop SQL query client.

There are already many SQL query clients on the market, so why develop a new one? The core reason is that existing SQL query clients generally have many pain points that affect user experience and work efficiency:

1. Lack of workspace isolation, resulting in table searches or scripts in the SQL console that cannot accurately target a specific database, leading to chaotic usage;

2. Tedious table search operations with low efficiency;

When a table has many fields, it is impossible to quickly locate the target column, requiring left and right dragging to find it, which is cumbersome and time-consuming;

4. Does not support visual charts such as line charts and bar charts, which are crucial for data analysis;

5. Cannot perform quick operations such as JSON formatting and URL Decode on column data;

6. Does not support quick hiding of columns;

7. Does not support custom code snippets in the SQL console, making it time-consuming to repeatedly write common scripts.

FrogDB provides efficient and convenient solutions to all the above pain points.

![logo](https://github.com/user-attachments/assets/eb1acca7-6a0c-466d-898e-a0f94d70a145)

## Product Overview

FrogDB is designed specifically for developers, data analysts, and DBAs who work with multiple databases every day.

Breaking away from the traditional model of treating SQL as isolated query windows, FrogDB offers a project-oriented workspace that supports reusable connection configurations, tabbed execution contexts, and fast data navigation.

Our goal is simple: reduce friction in daily database operations while maintaining control and security.

![demo](https://github.com/user-attachments/assets/b1da0ef0-16a2-43bd-8c57-b076888cf2d0)

## Features

### Database-Level Workspaces

Supports opening multiple databases simultaneously, with each database having an isolated workspace to avoid operational chaos.

![image](https://github.com/user-attachments/assets/dcdc46d7-edf1-46b0-8b2b-8026529d5be6)

After entering a database workspace, double-click the Shift key or click the search button in the upper right corner to quickly search all tables in that database.

![image](https://github.com/user-attachments/assets/0b452be6-731e-470f-ad8d-532f7ac16894)

When a table is open, press the shortcut key Command+O (Ctrl+F12 for Windows) to quickly jump to the target table column. This shortcut is the same as that in JetBrains IDEA, requiring no additional learning and zero usage cost.

![image](https://github.com/user-attachments/assets/dd38dfed-3564-4e14-9a8c-00583c40c81f)

### Remember Query History

In the WHERE condition edit box, you can directly select historical query records without retyping, which is convenient and efficient.

![image](https://github.com/user-attachments/assets/b0e27f01-8142-4a7d-acf2-b103b74f975d)

### Quick DDL Viewing

Click the "View DDL" button in the upper right corner to quickly view the DDL statement of the current table without manually writing queries.

![image](https://github.com/user-attachments/assets/ffd29311-bc14-46ca-bf95-05d9a7338c2f)

### View Row Data

Double-click the row number to view the complete data of the current row without switching views.

![image](https://github.com/user-attachments/assets/a3f31706-79a2-474d-82ac-bf6f206cbd11)

### View Cell Data

Double-click a cell to quickly view its details, which also supports data formatting for various formats such as JSON and URL.

![image](https://github.com/user-attachments/assets/1684f572-a5a1-4e9c-aa8d-36482277675c)

### Quick SQL Statement Generation

The "Copy as IN Query" function can quickly generate IN condition statements, facilitating batch query of target cell values, as shown in the example below:

```sql

IN ('luanqibazao')

```

The "Copy as Update" function can accurately generate update statements for a single field. Unlike other SQL tools that default to generating update statements for all fields (which require copying and manual modification), this function eliminates the need for manual edits and greatly improves efficiency, as shown in the example below:

```sql

UPDATE `uto_config` SET `type` = 'luanqibazao' WHERE `id` = 13;

```

![image](https://github.com/user-attachments/assets/e3b9811c-0502-40a5-8b7a-2a202653da8b)

If you need to generate INSERT, UPDATE, and DELETE statements for the entire row of records, right-click the row number and select copy, as shown in the example below:

![image](https://github.com/user-attachments/assets/004f2758-451e-41c7-b28a-5930f4d38ff6)

The generated SQL statements are as follows:

```sql

INSERT INTO `uto_config` (`cfg`, `created_at`, `id`, `type`, `updated_at`) VALUES (NULL, '2025-06-18 16:30:39', 13, 'luanqibazao', '2025-06-18 16:30:39');

UPDATE `uto_config` SET `cfg` = NULL, `created_at` = '2025-06-18 16:30:39', `id` = 13, `type` = 'luanqibazao', `updated_at` = '2025-06-18 16:30:39' WHERE `id` = 13;

DELETE FROM `uto_config` WHERE `id` = 13;

```

### Quick Column Hiding

Supports quick hiding of redundant table columns to focus on core data and improve viewing efficiency.

![image](https://github.com/user-attachments/assets/adad0f3c-54d5-40eb-89a7-6322d5822b26)

### Quick Result Search

Supports quick filtering of query results to accurately locate target data without re-executing the query.

![image](https://github.com/user-attachments/assets/ea97e6ca-cd43-47ee-bf18-d4c18fd5381a)

### Script Support

Supports script saving, allowing common scripts to be called at any time to avoid repeated writing.

![image](https://github.com/user-attachments/assets/7d21b944-e551-41a4-9203-ab15b8277bdd)

Supports adding custom code snippets, allowing quick insertion of common SQL snippets to improve writing efficiency.

![image](https://github.com/user-attachments/assets/b211d7e3-fc5f-4d32-9a71-3b8fdfb3926f)

### Chart Support

Built-in chart functionality supports various visualization forms such as line charts and bar charts to facilitate efficient data analysis.

![image](https://github.com/user-attachments/assets/6ad790cb-1fa3-45b0-830e-4966c962d875)

### Others

FrogDB also includes many user-friendly features waiting for you to explore:

- Multi-connection workspace with support for persistent connection configuration files, eliminating the need for repeated configuration;

- Support for optional SSH tunnel configuration to achieve secure remote database access;

- Read-only protection mode to block high-risk operations such as deletion and modification, ensuring data security;

- Monaco-based SQL editor providing a familiar and efficient coding experience;

- Convenient database and table exploration with result panels and row-level detail views;

- Support for script and query workflows with tabbed project context management;

- Rich visual UX enhancements, such as search panels, filtering tools, and quick navigation dialogs;

- More practical features, continuously updated.

## Core Advantages

- Optimize daily SQL workflows with an integrated workspace instead of scattered tools, improving collaboration and operational efficiency;

- Provide better operational security for sensitive environments through built-in read-only controls;

- Manage database connections, scripts, and results in one UI, reducing context switching costs;

- Cross-platform delivery model supporting teams running mixed operating systems.

## Typical Use Cases

- Investigate production environment issues through secure read-only query sessions to avoid misoperations;

- Develop and verify SQL scripts across multiple architectures to ensure compatibility;

- Explore unfamiliar database structures through quick table/data checks to improve cognitive efficiency;

- Manage periodic analysis and ad-hoc query tasks in a reusable workspace to improve reusability.

## Product Positioning

FrogDB is positioned as a productivity-focused MySQL desktop client: powerful yet lightweight, supporting advanced SQL workflows, suitable for daily use, and adhering to a safe and efficient execution philosophy to provide a better operating experience for database professionals.
