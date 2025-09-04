# Zion Cursor Rules

Zion 平台代码组件开发的 Cursor AI 规则库，提供完整的开发流程指导和代码规范。

## 📋 规则文件说明

### 核心规则文件

| 文件名 | 描述 | 用途 |
|--------|------|------|
| `zion-master-controller.mdc` | 主控制器 | 智能模式控制和流程调度 |
| `zion-requirement-refinement.mdc` | 需求完善流程 | 通过智能提问完善组件需求 |
| `zion-development-workflow.mdc` | 开发执行流程 | 15步标准开发流程 |
| `zion-code-standards.mdc` | 代码规范 | 三段式接口标准和文件结构 |
| `zion-graphql-schema-guide.mdc` | GraphQL 架构指南 | Schema 结构和 API 查询规范 |

## 🚀 快速开始

### 1. 安装规则到 Cursor

将规则文件复制到您的 Cursor 项目的 `.cursor/rules/` 目录：

```bash
# 复制所有规则文件
cp *.mdc /path/to/your/project/.cursor/rules/
```

### 2. 使用规则

在 Cursor 中，这些规则会自动生效。您可以通过以下方式使用：

- **开始新组件开发**: 直接描述您的组件需求
- **生成开发计划**: 输入 `PLAN`
- **执行开发流程**: 输入 `ACT`

## 🎯 开发流程

### REQUIREMENT 模式
- 触发条件：用户提出新组件开发需求
- 执行动作：开始需求完善流程，逐步收集详细信息

### PLAN 模式
- 触发条件：用户输入 "PLAN"
- 执行动作：生成详细的开发计划和技术方案

### ACT 模式
- 触发条件：用户输入 "ACT"
- 执行动作：执行15步标准开发流程

## 📚 规则详解

### 主控制器 (zion-master-controller.mdc)
- 智能模式识别与流程调度
- 项目状态检测机制
- 异常处理和恢复策略

### 需求完善 (zion-requirement-refinement.mdc)
- 8步完善流程
- 智能提问原则
- 分类调整逻辑（语音转换、数据展示、表单操作、文件上传、图表统计等）

### 开发流程 (zion-development-workflow.mdc)
- 15步标准开发流程
- 环境配置和项目管理
- 代码实现和发布部署

### 代码规范 (zion-code-standards.mdc)
- 三段式接口规范：PropData、StateData、Event、Props
- 文件结构和导出规范
- 组件集成标准

### GraphQL 指南 (zion-graphql-schema-guide.mdc)
- Schema 结构说明
- API 查询规范
- 媒体上传协议

## 🔧 自定义和扩展

### 添加新规则
1. 创建新的 `.mdc` 文件
2. 在 `zion-master-controller.mdc` 中引用
3. 更新本 README 文档

### 修改现有规则
1. 直接编辑对应的 `.mdc` 文件
2. 保持文件格式和结构一致
3. 测试规则是否正常工作

## 📝 版本历史

- **v3.0** - 添加图表统计类 ECharts 支持
- **v2.0** - 完善需求收集流程
- **v1.0** - 初始版本发布

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

---

**注意**: 这些规则专为 Zion 平台代码组件开发设计，请确保在正确的环境中使用。
