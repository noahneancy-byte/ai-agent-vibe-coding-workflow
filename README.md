# AI Agent Vibe Coding Workflow Skill

一个面向 AI Agent 产品全流程交付的 Codex Skill 组合包。它把三份独立手册串成统一工作流：

**通用开发 → 正式前端 → 上线部署**

`SKILL.md` 只负责判断任务阶段、路由到对应手册并约束阶段衔接；三份原始 Markdown 手册完整保存在 `references/` 中，正文未作改写。

## 适用场景

- 从 PRD 和技术适配开始搭建 AI Agent MVP
- 开发或完善 Agent 核心链路与后端能力
- 在核心链路通过验证后建设正式 Web 前端
- 设计 Agent 运行状态、流式反馈与响应式交互
- 将前后端部署到生产环境并完成线上验收
- 贯通从需求、开发、前端到上线的完整交付流程

## 工作流

| 阶段 | 典型任务 | 路由文件 |
| --- | --- | --- |
| 1. 通用开发 | PRD、技术适配、MVP、Agent 核心链路、后端与核心验收 | `references/AI产品Vibe Coding通用技术栈手册.md` |
| 2. 正式前端 | Web 前端、组件、Agent 状态交互、响应式与前端验收 | `references/AI产品Vibe Coding通用前端技术栈手册.md` |
| 3. 上线部署 | 火山引擎、鉴权、持久化、存储、监控、发布与线上验收 | `references/AI Agent 产品上线部署手册.md` |

完整任务按阶段顺序推进；单阶段任务只加载相关手册，同时检查必要的上游条件。

## 目录结构

```text
ai-agent-vibe-coding-workflow/
├── SKILL.md
├── README.md
└── references/
    ├── AI产品Vibe Coding通用技术栈手册.md
    ├── AI产品Vibe Coding通用前端技术栈手册.md
    └── AI Agent 产品上线部署手册.md
```

## 安装

将仓库克隆或复制到 Codex 的个人技能目录：

```bash
git clone <repository-url> ~/.codex/skills/ai-agent-vibe-coding-workflow
```

重新打开相关任务后即可通过自然语言自动触发，也可以显式指定：

```text
$ai-agent-vibe-coding-workflow
```

## 使用示例

```text
用 $ai-agent-vibe-coding-workflow 根据这份 PRD 先完成技术适配和 MVP 核心链路。
```

```text
用 $ai-agent-vibe-coding-workflow 在现有 Agent 后端上建设正式 Web 前端，并按手册验收。
```

```text
用 $ai-agent-vibe-coding-workflow 检查当前项目的上线条件，并部署到生产环境。
```

## 内容边界

- `SKILL.md` 是路由与执行入口，不复制三份手册正文。
- `references/` 中的三个文件是原始资料，应保持原文不变。
- 实际执行以用户当前请求为范围；进入某一阶段不代表自动授权生产发布或其他外部变更。
