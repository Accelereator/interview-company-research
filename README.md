# Interview Company Research

一个面向**求职者**的 Claude Code Skill，在面试前对目标公司做系统性深度调研，输出一份可直接阅读的 HTML 报告。

> 当前版本侧重 AIPM（AI 产品经理）岗位的面试场景，技术问题主题为 Agent / MCP / 评估 / 端侧约束 / Badcase / 数据 Owner。其他岗位可基于 `references/question-design.md` 自行调整技术主题。

## ✨ 能做什么

输入一张 BOSS 直聘岗位截图 + 你的简历，自动产出包含以下章节的 HTML 报告：

- **岗位画像** + JD 拆解 + 能力需求权重
- **候选人 Fit 分析**（核心差异化）：基于你的简历做"强 / 弱 / Gap"三段对照，每项给出"证据 + 面试时怎么应对"
- **企业基本信息 / 主要业务 / 主要产品**（强制 WebSearch，标注时效）
- **竞品对比** + 明确的优势落点判断
- **12 个面试预设问题**（业务 6 + 技术 6），每题三段式答案
- **3-5 个有深度的反问问题**

## 📦 安装

```bash
# 克隆到 Claude Code 的 skills 目录
cd ~/.claude/skills/
git clone https://github.com/你的用户名/interview-company-research.git
```

重启 Claude Code 后，skill 会自动被识别。

## 🚀 使用方法

1. 在工作目录下创建 `简历/` 文件夹，放入你的简历（PDF / Markdown / Word 均可）
2. 在 Claude Code 中粘贴一张 BOSS 直聘岗位截图
3. 说"帮我调研一下这家公司"或"我要面试这家公司"
4. Skill 自动触发，几分钟后浏览器会打开生成的 HTML 报告

报告默认保存到 `./reports/{公司简称}-{岗位}-{YYYY-MM-DD}.html`

## 🎯 设计原则

- **真实优先**：所有公司信息走 WebSearch，不依赖训练数据
- **官方源优先**：官网 / 财报 / CEO 演讲 > 媒体 > 自媒体
- **诚实标 Gap**：简历与岗位不匹配时，给迁移说明而不是假装全匹配
- **优势导向**：竞品对比必须给出"面试公司差异化优势"的明确判断

## 📁 项目结构

```
interview-company-research/
├── SKILL.md                          # 主入口，定义工作流
├── references/
│   ├── search-strategy.md            # 搜索策略与信息源分级
│   ├── question-design.md            # 12 个问题的设计方法
│   └── competitor-analysis.md        # 竞品对比与优势落点
└── assets/
    └── template.html                 # 报告 HTML 模板
```

## ⚠️ 注意事项

- 需要联网（WebSearch 工具权限）
- 简历内容只在本地处理，不会上传到任何外部服务
- 报告里所有信息都基于公开 WebSearch 结果，使用前请自行验证关键数据

## 📄 License

MIT
