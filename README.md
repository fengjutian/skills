# Skills

一套面向 Python + Vue 全栈系统的智能分析与重构技能集合，支持代码审查、业务梳理与架构重构，按阶段递进使用。

---

## 技能列表

| 阶段 | Skill | 类型 | 说明 |
|------|-------|------|------|
| Stage 1 | [code-reviewer](#code-reviewer) | analysis | 代码审查，发现 Bug / 性能 / 安全问题 |
| Stage 2 | [system-business-deep-dive](#system-business-deep-dive) | analysis | 业务梳理，还原系统业务流程与数据流 |
| Stage 3 | [system-refactor-designer](#system-refactor-designer) | design | 架构重构，输出可执行的系统重构方案 |

> 三个技能存在依赖关系，建议按阶段顺序使用以获得最佳效果。

---

## code-reviewer

**角色**：资深 Python + Vue 全栈代码审计专家

**适用输入**：Python / FastAPI / Django / Flask 代码、Vue / Pinia / Vuex 代码、SQL 语句、API 接口定义

**分析维度**：
- 代码规范（命名、结构、可读性）
- 潜在 Bug（空值、边界、异常处理）
- 性能问题（N+1 查询、循环 DB 访问）
- 安全问题（SQL 注入、权限绕过、信息泄露）
- 架构问题（Service 过重、模块耦合）

**输出**：问题清单 + 风险等级（P0/P1/P2）+ 优化建议 + 修复示例

---

## system-business-deep-dive

**角色**：资深全栈系统架构师，擅长从代码还原完整业务系统

**依赖**：建议先执行 `code-reviewer`

**适用输入**：后端代码、前端页面/组件、数据库表结构、接口定义、业务描述

**分析维度**：
- 业务目标（模块解决的问题、服务对象、输入/输出）
- 系统角色（管理员、用户、第三方、内部服务）
- 系统结构（前端模块、后端 API、Service 层、DB、外部依赖）
- 核心业务流程（Mermaid 流程图）

---

## system-refactor-designer

**角色**：资深系统架构师，专注高并发设计、微服务拆分与系统重构

**依赖**：建议先执行 `system-business-deep-dive`

**适用输入**：代码结构、API、数据库表结构、业务流程、前两阶段输出结果

**输出内容**：
1. 当前架构问题分析（架构层 / 数据层 / 调用链 / 系统问题）
2. 重构目标定义（模块解耦、服务拆分、性能提升等）
3. 新架构设计（Mermaid 架构图）
4. 数据库优化方案
5. 分阶段落地路径

---

## 使用流程

```
代码 / 数据库 / 接口
        │
        ▼
 [Stage 1] code-reviewer
   → 发现代码级问题
        │
        ▼
 [Stage 2] system-business-deep-dive
   → 还原业务逻辑与系统结构
        │
        ▼
 [Stage 3] system-refactor-designer
   → 输出系统重构方案
```
