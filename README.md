# JC-Skills

个人 OpenCode 技能集合，每个技能是一个独立的 `SKILL.md` 文件，由 OpenCode 通过 `skill` 工具加载。

## 目录结构

```
skills/<skill-name>/SKILL.md
```

纯内容仓库，无构建系统、无测试、无 CI。

## 已有技能

| 技能 | 用途 |
|---|---|
| `codex-token-summary` | 统计本机 Codex token 消耗，按任务目的、模型维度输出中文表格 |
| `project-sess-summary` | 项目会话记忆管理，基于 `jcemb` 向量工具实现对话总结、检索、上下文延续 |

## 添加新技能

1. 创建 `skills/<skill-name>/SKILL.md`
2. YAML frontmatter 至少包含 `name` 和 `description`
3. 目录名与 frontmatter 中的 `name` 保持一致
4. 内容用中文编写

详见 `AGENTS.md`。
