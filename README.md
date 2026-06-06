# SDD Vibe Coding Pro（专业版）

> 面向产品经理的规范驱动开发（SDD）AI 编程 Skill —— 专业版。

## 这是什么？

SDD Vibe Coding Pro 是一套给 AI 编程 Agent（如 Claude Code、Cursor、Copilot）使用的**工作流 Skill**。它将你的角色从"不懂代码的产品经理"转变为"项目指挥官"——你只需要确认需求和验收，AI 按照严格的工程纪律完成开发。

## 基础版 vs 专业版

| 特性 | 基础版 | 专业版 |
|------|--------|--------|
| 规范文档 | 简化的 5 份文档 | 5 份正式文档 + 评审重点 |
| Harness 验证 | 自检 | Lint → Type → Test → Build 四层链 |
| TDD | 建议 | 强制（红绿循环） |
| Git 分支 | 不提 | main 锁定 + milestone-x 分支 |
| 自愈机制 | 3 次修复上限 | Auto-Heal 3 轮 + A/B/C 升级选项 |
| 日志 | 无 | /logs/YYYY-MM-DD.md |
| 交付 | 简单 Checklist | DEPLOY/README/CHANGELOG/review 全套 |

## 四阶段工作流

```
Phase 1: 需求澄清       → /docs/confirmation.md + 5 份规范文档
Phase 2: 制定规划       → 里程碑拆分 + 脚手架 + 分支管理
Phase 3: 增量开发       → TDD + Harness 四层验证 + Auto-Heal
Phase 4: 交付与复盘     → 上线 Checklist + 项目复盘 + UAT 验收
```

## 安装

### 方法 1：直接导入 .skill 文件

1. 下载 `sdd-vibe-coding-pro.skill`
2. 在 Claude Code 中运行：`/skill:install <path-to-.skill-file>`

### 方法 2：手动安装

将 `sdd-vibe-coding-pro/` 目录复制到 `~/.claude/skills/` 下。

### 方法 3：Git Clone

```bash
git clone https://github.com/<your-username>/sdd-vibe-coding-pro.git
cp -r sdd-vibe-coding-pro/sdd-vibe-coding-pro ~/.claude/skills/
```

## 触发方式

在 Claude Code 中输入类似以下内容即可触发：

- "我想用专业版 SDD 流程开发一个 XX 系统"
- "帮我按严格模式做一个 XX 应用，需要分支管理和测试覆盖"
- "用 SDD Pro 开发一个企业级 XX 平台"

也支持 `/sdd-vibe-coding-pro` 直接调用。

## 适用场景

- 企业/团队内部工具（权限管理、多角色、数据库）
- 需要多模块、多迭代的正式项目
- 对质量有较高要求的软件产品
- 想在 Vibe Coding 中引入工程纪律的产品经理

## 核心工程实践

- **Spec-First**：先写规范文档，确认后才写代码
- **TDD**：先写失败测试，再写实现
- **Harness 四层验证**：Lint → Type → Test → Build
- **Git 分支保护**：main 锁定，milestone 分支开发
- **Auto-Heal**：自愈 3 轮上限，超限升级 A/B/C 方案
- **暂停硬停止**：用户随时说"暂停"，立刻停止

## 用户指令速查

| 你说 | 含义 |
|------|------|
| 「规范评审通过」 | 确认方案，进入开发计划 |
| 「开始开发」 | 启动增量开发 |
| 「开发」 | 同意当前子任务 |
| 「继续」 | 做下一个子任务 |
| 「演示」 | 看当前效果 |
| 「合并」 | 里程碑确认，合并到 main |
| 「暂停」 | 紧急停止当前所有工作 |

## 作者

由产品经理实战总结的 Vibe Coding 工作流，适用于日常工作中与 AI 编程 Agent 协作。

## License

MIT
