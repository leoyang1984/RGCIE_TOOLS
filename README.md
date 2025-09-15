# RGCIE Tools - YAML提示词创作框架

[![GitHub](https://img.shields.io/github/license/leoyang1984/RGCIE_TOOLS)](https://github.com/leoyang1984/RGCIE_TOOLS)
[![GitHub issues](https://img.shields.io/github/issues/leoyang1984/RGCIE_TOOLS)](https://github.com/leoyang1984/RGCIE_TOOLS/issues)
[![GitHub stars](https://img.shields.io/github/stars/leoyang1984/RGCIE_TOOLS)](https://github.com/leoyang1984/RGCIE_TOOLS/stargazers)

RGCIE Tools 是一个专门用于创建结构化YAML提示词的框架，基于RGCIE（Role-Goals-Constraints-Instructions-Examples）原则设计，旨在帮助用户创作高质量的AI提示词。

## 📖 目录

- [项目介绍](#-项目介绍)
- [RGCIE框架](#-rgcie框架)
- [🛠️ 安装和使用](#️-安装和使用)
- [📁 项目结构](#-项目结构)
- [🎯 核心功能](#-核心功能)
- [📋 示例](#-示例)
- [🤝 贡献指南](#-贡献指南)
- [📄 许可证](#-许可证)
- [📞 联系方式](#-联系方式)

## 🚀 项目介绍

RGCIE Tools 提供了一个系统化的方法来创建结构化提示词，通过RGCIE框架确保提示词的完整性、一致性和有效性。这个框架特别适合：

- AI提示词工程师
- 开发者需要与AI模型交互
- 技术写作人员
- 任何需要创建高质量提示词的用户

## 🎯 RGCIE框架

RGCIE是一个结构化的提示词创作原则，包含五个核心要素：

### R - Role (角色)
定义AI模型应该扮演的角色和身份

### G - Goals (目标)
设定AI模型需要达成的具体目标

### C - Constraints (约束)
明确行为边界和限制条件

### I - Instructions (指令)
提供具体的操作指南和执行步骤

### E - Examples (示例)
通过实例来具体化抽象指导

### 高级特性

#### 嵌套结构
支持RGCIE的嵌套使用，创建更精细的提示词结构

#### 模块化设计
提供多种补充模块来处理复杂场景：
- 知识模块 (Knowledge Base)
- 输出格式模块 (Output Format)
- 条件处理模块 (Conditional Handling)
- 专业化模式模块 (Specialized Modes)
- 评估反馈模块 (Evaluation & Feedback)

## 🛠️ 安装和使用

### 环境要求
- 任何支持YAML的文本编辑器
- 基本的YAML语法知识

### 快速开始

1. **克隆项目**
```bash
git clone https://github.com/leoyang1984/RGCIE_TOOLS.git
cd RGCIE_TOOLS
```

2. **查看示例**
查看 `测试样例/` 目录中的示例文件：
- `code_review_prompt.yaml` - 完整的代码审查提示词示例
- `test_prompt_request.md` - 提示词需求文档示例

3. **创建你的提示词**
参考示例文件的结构，使用RGCIE框架创建你自己的提示词。

### 使用流程

1. **定义需求**：明确你的提示词需要实现什么功能
2. **应用RGCIE**：按照Role→Goals→Constraints→Instructions→Examples的顺序结构化
3. **选择模块**：根据需要添加适当的补充模块
4. **验证语法**：确保YAML语法正确
5. **测试优化**：在实际场景中测试并优化提示词

## 📁 项目结构

```
RGCIE_TOOLS/
├── 测试样例/                 # 示例文件
│   ├── code_review_prompt.yaml    # 代码审查提示词示例
│   └── test_prompt_request.md     # 提示词需求文档
├── 过程文件/                 # 过程文档
│   ├── yaml提示词创作助手.md      # RGCIE框架详细说明
│   └── cline_memory_bank_zh.md    # 项目记忆库
└── README.md                # 项目说明文档
```

## 🎯 核心功能

### 1. 结构化提示词创作
- 基于RGCIE原则的系统化方法
- 确保提示词的完整性和一致性
- 支持复杂的嵌套结构

### 2. 模块化扩展
- 知识模块：领域专业知识集成
- 输出格式：响应结构化控制
- 条件处理：多场景适应性
- 专业化模式：角色切换和能力聚焦

### 3. 质量保证
- 语法验证和完整性检查
- 实用性评估标准
- 持续优化机制

### 4. 教育价值
- 提供最佳实践示例
- 详细的框架说明
- 实际应用案例

## 📋 示例

### 基础RGCIE结构示例

```yaml
role: 资深代码审查专家
goals:
  primary:
    - 识别代码中的潜在问题和bug
    - 提供具体的改进建议
  secondary:
    - 教育开发者理解问题原因

constraints:
  - 保持专业和建设性的语气
  - 重点关注重要问题而非风格细节

instructions:
  - 按优先级分类问题
  - 为每个问题提供解释和修复建议

examples:
  memory_leak:
    scenario: "内存泄漏检测示例"
    problem_code: "问题代码示例"
    fixed_code: "修复后代码示例"
```

### 完整示例
查看 `测试样例/code_review_prompt.yaml` 获取完整的代码审查提示词示例。

## 🤝 贡献指南

我们欢迎任何形式的贡献！请参考以下指南：

### 如何贡献

1. **Fork 项目**
2. **创建特性分支** (`git checkout -b feature/AmazingFeature`)
3. **提交更改** (`git commit -m 'Add some AmazingFeature'`)
4. **推送到分支** (`git push origin feature/AmazingFeature`)
5. **开启 Pull Request**

### 贡献规范

- 遵循现有的代码风格和文档格式
- 确保YAML语法正确性
- 提供充分的示例和文档
- 测试你的更改在实际场景中的效果

### 报告问题

如果你发现任何问题或有改进建议，请：
1. 查看现有issue是否已经报告
2. 创建新的issue，提供详细描述和重现步骤
3. 如果可能，提供修复建议或示例代码

## 📄 许可证

本项目采用 MIT 许可证 - 查看 [LICENSE](LICENSE) 文件了解详情。

## 📞 联系方式

- **项目维护者**: [leoyang1984](https://github.com/leoyang1984)
- **项目地址**: [https://github.com/leoyang1984/RGCIE_TOOLS](https://github.com/leoyang1984/RGCIE_TOOLS)
- **问题反馈**: [创建Issue](https://github.com/leoyang1984/RGCIE_TOOLS/issues)

## 🔮 未来发展

- [ ] 更多领域特定的提示词模板
- [ ] 可视化提示词创作工具
- [ ] 提示词效果评估系统
- [ ] 社区贡献指南完善
- [ ] 多语言支持扩展

---

⭐ 如果这个项目对你有帮助，请给它一个star！你的支持是我们持续改进的动力。
