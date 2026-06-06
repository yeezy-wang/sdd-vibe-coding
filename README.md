# SDD Vibe Coding

> 面向产品经理的规范驱动开发（SDD）AI 编程 Skill —— 让不懂代码的 PM 也能指挥 AI 完成严格工程纪律的项目开发。

## 这是什么？

SDD Vibe Coding 是一套给 AI 编程 Agent（如 Claude Code、Cursor、Copilot）使用的**工作流 Skill**。它将你的角色从"不懂代码的产品经理"转变为"项目指挥官"——你只需确认需求和验收，AI 按照严格的工程纪律完成所有技术工作。

## 四阶段工作流

```
Phase 1: 需求澄清       → /docs/confirmation.md + 5 份规范文档
Phase 2: 制定规划       → 里程碑拆分 + 脚手架 + 分支管理
Phase 3: 增量开发       → TDD + Harness 四层验证 + Auto-Heal
Phase 4: 交付与复盘     → 上线 Checklist + 项目复盘 + UAT 验收
```

## 安装

### 方法 1：直接导入 .skill 文件

1. 下载 `sdd-vibe-coding.skill`
2. 在 Claude Code 中运行：`/skill:install <path-to-.skill-file>`

### 方法 2：手动安装

将 `sdd-vibe-coding/` 目录复制到 `~/.claude/skills/` 下。

### 方法 3：Git Clone

```bash
git clone https://github.com/yeezy-wang/sdd-vibe-coding.git
cd sdd-vibe-coding && cp -r sdd-vibe-coding ~/.claude/skills/
```

## 触发方式

在 Claude Code 中输入类似以下内容即可触发：

- "我想开发一个 XX 系统，帮我按 SDD 流程来做"
- "帮我做一个 XX 应用，需要分支管理、测试覆盖和里程碑拆分"
- "我想从零开始认真开发一个 XX 产品"

也支持 `/sdd-vibe-coding` 直接调用。

## 适用场景

- 企业/团队内部工具（权限管理、多角色、数据库）
- 需要多模块、多迭代的正式项目
- 对质量有较高要求的软件产品
- 想在 Vibe Coding 中引入工程纪律的产品经理

## 核心工程实践

- **Spec-First**：5 份规范文档评审通过后才写代码
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
