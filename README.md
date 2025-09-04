# Zion Cursor Rules

Zion 平台开发的用Cursor生成 Zion 代码组件的规则库，基于用户一句话需求，通过智能模式控制，自动化完成 Zion 组件的完整开发流程。

## 📋 规则文件说明

### 核心规则文件

| 文件名 | 描述 | 用途 | 状态 |
|--------|------|------|------|
| `zion-master-controller.mdc` | 主控制器 v3.0 | 智能模式控制和流程调度 | ✅ 自动应用 |
| `zion-requirement-refinement.mdc` | 需求完善流程 | 8步智能提问完善组件需求 | 🔄 按需调用 |
| `zion-development-workflow.mdc` | 开发执行流程 | 15步标准开发流程 | 🔄 按需调用 |
| `zion-code-standards.mdc` | 代码规范 | 三段式接口标准和文件结构 | 🔄 按需调用 |
| `zion-graphql-schema-guide.mdc` | GraphQL 架构指南 | Schema 结构和 API 查询规范 | 🔄 按需调用 |

## 🚀 快速开始

### 1. 安装规则到 Cursor

将规则文件复制到您的 Cursor 项目的 `.cursor/rules/` 目录：

```bash
# 复制所有规则文件
cp cursor-rules/*.mdc /path/to/your/project/.cursor/rules/
```

### 2. 使用规则

在 Cursor 中，主控制器规则会自动生效。您可以通过以下方式使用：

- **开始新组件开发**: 直接描述您的组件需求（自动触发 REQUIREMENT 模式）
- **生成开发计划**: 输入 `PLAN`（触发 PLAN 模式）
- **执行开发流程**: 输入 `ACT`（触发 ACT 模式）

## 🎯 智能模式控制

### REQUIREMENT 模式
- **触发条件**: 用户提出新组件开发需求，需求描述不够详细或完整
- **执行动作**: 立即开始执行需求完善流程的第一步，按照"一次一问"原则逐步完善需求
- **完成标志**: 提示用户输入 "PLAN" 生成开发计划

### PLAN 模式
- **触发条件**: 用户完成需求完善流程，用户输入 "PLAN"，需要技术方案确认
- **执行动作**: 生成详细的开发计划和技术方案，包含需求分析、项目规划、技术方案和执行步骤
- **完成标志**: 提示用户输入 "ACT" 确认执行此计划

### ACT 模式
- **触发条件**: 用户输入 "ACT"，用户提出直接的操作请求
- **执行动作**: 执行15步标准开发流程，从环境验证到发布上线
- **完成标志**: 组件开发完成并成功发布

## 📚 规则详解

### 主控制器 (zion-master-controller.mdc)
- **智能模式识别**: 自动识别用户意图，调度相应流程
- **项目状态检测**: 智能检测现有项目，避免目录混乱
- **异常处理机制**: 自动重试、错误恢复、断点续跑
- **核心约束**: 目录唯一性原则，严格遵循Zion平台规范

### 需求完善 (zion-requirement-refinement.mdc)
- **8步完善流程**: 从组件基础信息到最终确认
- **智能提问原则**: 一次一问、简单直接、智能提取、循序渐进
- **分类调整逻辑**: 支持语音转换、数据展示、表单操作、文件上传、图表统计等
- **图表库支持**: 推荐 ECharts、Chart.js、D3.js、AntV G2、Recharts 等

### 开发流程 (zion-development-workflow.mdc)
- **15步标准流程**: 从环境验证到发布上线的完整流程
- **环境配置**: Node.js、Functorz CLI、tsx 等工具验证与安装
- **项目管理**: 项目状态检查、依赖安装、MCP 配置获取
- **代码实现**: 目录文件生成、代码实现、组件集成
- **发布部署**: 本地测试、预览测试、平台发布

### 代码规范 (zion-code-standards.mdc)
- **三段式接口规范**: PropData、StateData、Event、Props 四个 interface
- **文件结构标准**: 统一的目录结构和命名规范
- **导出规范**: 标准化的组件导出和集成方式
- **React 原则**: 全部使用 React，严格遵循 props 协议

### GraphQL 指南 (zion-graphql-schema-guide.mdc)
- **Schema 结构**: 完整的数据库结构说明
- **API 查询规范**: GraphQL 查询语法和最佳实践
- **媒体上传协议**: 图片、视频、文件上传的专用流程
- **MCP 工具集成**: 与 Zion 平台的深度集成

## 🔧 自定义和扩展

### 添加新规则
1. 在 `cursor-rules/` 目录下创建新的 `.mdc` 文件
2. 在 `zion-master-controller.mdc` 中引用新规则
3. 更新本 README 文档和 CHANGELOG.md

### 修改现有规则
1. 直接编辑 `cursor-rules/` 目录下对应的 `.mdc` 文件
2. 保持文件格式和结构一致
3. 测试规则是否正常工作
4. 更新版本号和 CHANGELOG.md

### 版本管理
- 使用语义化版本号 (Semantic Versioning)
- 重大更新：v3.0.0
- 功能新增：v3.1.0
- 问题修复：v3.0.1

## 🤝 贡献指南

1. Fork 本仓库
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 开启 Pull Request

## 📄 许可证

本项目采用 MIT 许可证 - 查看 [LICENSE](LICENSE) 文件了解详情。

## 🆘 支持

如果您在使用过程中遇到问题，请：

1. 查看 [Issues](../../issues) 中是否有类似问题
2. 创建新的 Issue 描述您的问题
3. 提供详细的错误信息和复现步骤

## 📝 版本历史

- **v3.0.0** - 添加图表统计类 ECharts 支持，完善智能模式控制
- **v2.0.0** - 完善需求收集流程，支持多种组件类型
- **v1.0.0** - 初始版本发布，基础规则体系

## 🎯 核心特性

- **智能模式控制**: 自动识别用户意图，调度相应开发流程
- **完整开发流程**: 从需求收集到发布上线的全自动化流程
- **标准化规范**: 严格遵循 Zion 平台的三段式接口规范
- **图表库支持**: 内置 ECharts 等主流图表库推荐
- **异常处理**: 自动重试、错误恢复、断点续跑机制
- **项目检测**: 智能检测现有项目，避免目录混乱

---

**注意**: 这些规则专为 Zion 平台代码组件开发设计，请确保在正确的环境中使用。使用前请确保已安装 Node.js v20.19.4 和 Functorz CLI。
