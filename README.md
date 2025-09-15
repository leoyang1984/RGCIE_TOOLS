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
- VS Code 编辑器
- Cline 插件
- 基本的YAML语法知识（可选）

### 快速开始

1. **下载项目**
   下载或克隆本项目到本地

2. **使用VS Code打开项目**
   使用VS Code打开RGCIE_TOOLS文件夹

3. **配置Cline Rules**
   有两种方式使用RGCIE提示词创作助手：
   
   **方式一：使用现有规则文件**
   - 项目已包含完整的规则文件：`过程文件/yaml提示词创作助手.md`
   - 将此文件复制到项目根目录的`.clinerules/`文件夹中（如不存在请创建）
   - 或者直接在VS Code中打开此文件参考使用

   **方式二：创建自定义规则**
   - 在项目根目录创建`.clinerules/`文件夹
   - 将`过程文件/yaml提示词创作助手.md`的内容复制到新的规则文件中
   - 根据需要自定义规则内容

4. **激活使用**
   - 安装并启用Cline插件
   - 在VS Code中，按照规则文件中的激活指令使用
   - 当输入包含以下关键词时自动激活RGCIE提示词创作功能：
     - "创作提示词"
     - "YAML提示词"  
     - "RGCIE框架"
     - "提示词优化"
     - "结构化提示"

### 使用流程

1. **触发激活**：输入包含激活关键词的提示词需求
2. **自动识别**：Cline自动检测并激活RGCIE提示词创作助手
3. **需求分析**：分析用户输入的提示词创作需求
4. **RGCIE结构化**：按照Role→Goals→Constraints→Instructions→Examples原则结构化
5. **生成YAML**：输出完整的YAML格式提示词
6. **优化建议**：提供使用建议和优化说明

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
