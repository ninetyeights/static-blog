---
title: MongoDB 基本操作
author: Rain
tags:
  - 学习笔记
  - MongoDB
categories:
  - 数据库
top_img: false
cover: false
date: 2022-03-02 20:15:28
---

> 官方网站：https://www.mongodb.com/

> 社区版下载链接：https://www.mongodb.com/try/download/community

### [如何安装 MongoDB](/)

### 关系型和非关系型数据库对比

| SQL 术语/概念 | MongoDB 术语/概念 | 解释/说明                             |
| ------------- | ----------------- | ------------------------------------- |
| database      | database          | 数据库                                |
| table         | collection        | 表/集合                               |
| row           | document          | 数据记录行/文档                       |
| column        | field             | 数据记录列/字段                       |
| index         | index             | 索引                                  |
| table joins   |                   | 表链接，MongoDB 不支持                |
| primary key   | primary key       | 主健，MongoDB 自动将\_id 字段设为主健 |

### 常用命令

| 命令             | 描述                                           |
| ---------------- | ---------------------------------------------- |
| help             | 显示帮助                                       |
| show databases   | 列出所有可用数据库                             |
| show dbs         | 列出所有数据库                                 |
| use \<db>        | 将当前数据库切换至 db                          |
| show collections | 列出当前数据库的所有集合                       |
| show users       | 列出当前数据库的用户列表                       |
| show roles       | 列出当前数据库的角色列表（包括自定义和内置的） |

### 创建用户

```sql
db.createUser({user: "chester", pwd: "chester0611", roles: [{role: "userAdmin", db: "admin"}], customData: {desc: "超级管理员用户, chester"}})
```

    db.createUser({
      user: "用户名",
      pwd: "密码",
      roles: [{
        role: "角色",
        db: "数据库"
      }],
      customData: {
        自定义字段
      }
    })
