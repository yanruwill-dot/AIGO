# MEMORY.md - Long-Term Memory

*Your curated memories. The distilled essence, not raw logs.*

## About This File & Memory System

- **Be mindful in shared contexts** — this file contains personal context about your human. In group chats or shared sessions, don't leak private preferences, decisions, or project details

### Three-Layer Memory

Your memory has three layers, each with different responsibilities and access patterns:

**Core memory (this file, 04-MEMORY.md)** — Auto-loaded every session
- What goes here: cross-project lessons, key decisions, user preferences, technical knowledge, one-line project summaries + pointers
- What doesn't: detailed project experience (that's what topic files are for)
- **Add a timestamp `(YYYY-MM-DD)` to each entry** — helps trace back, judge recency, clean up

**Topic memory (`memory/topics/<name>.md`)** — Read before working on a project
- What goes here: full accumulated experience for one project/topic — status, key facts, what you did, what worked, what didn't, decisions and rationale, next steps
- More detailed than core memory (which only has pointers), more synthesized than daily logs (which are raw chronological notes)
- Update during memory maintenance or when a project enters a new phase

**Daily journal (`memory/YYYY-MM-DD.md`)** — Read today + yesterday at session start
- What goes here: what happened that day, raw chronological record
- This is the source of all memory, but searching it for specific info is inefficient

### When to Read What

- Just woke up → this file is already loaded + read today/yesterday's logs
- About to work on a project → read its `memory/topics/<name>.md`
- Memory maintenance → read all recent logs + all active topic files

---

## Lessons Learned

### Working Style (2026-03-31)

- Will 不喜欢废话，一句话能搞定的别用三句
- 不确定就问，不要猜
- 本地可逆操作默认直接做，不反复确认
- 成果优先于过程 —— 先产出可检查物，再汇报

### Communication (2026-03-31)

- 中文为主，代码和技术术语保持英文
- 脏话可以用但别刻意
- "很好的问题""很高兴能帮到你"是禁句
- 错了就认，别嘴硬

### Technical (2026-03-31)

- 设计风格：Apple/Tesla 极简，拒绝低龄化
- 不从零造轮子，先搜 GitHub
- 增量开发，写完就测
- macOS 开发用 Swift/AppKit，不用 pynput

## Important Decisions

*(Record key decisions and their reasoning here.)*

## User Preferences

*(What you've learned about how your human likes to work.)*

- 见 03-USER.md 完整记录

## Technical Knowledge

### MyAgents 架构 (2026-03-31)

- 三层架构：React 前端 → Rust 代理层 → Bun Sidecar 后端
- 每个 Chat Session 有独立 Sidecar 进程
- MCP 工具通过 Sidecar 调用
- Agent Channel：Telegram/钉钉内置，微信通过 OpenClaw 社区插件

### 企业微信机器人配置 (2026-03-31)

- 插件：`@tencent-weixin/openclaw-weixin`
- 平台：https://ilinkai.weixin.qq.com
- 需要在 MyAgents 设置里扫码登录绑定账号
- 不是普通联系人，是"智能链接"服务的应用机器人

## Ongoing Context

### MyAgents 企业微信接入 (2026-03-31)

- 插件已安装，账号已扫码绑定
- Agent "天才" 已启用微信 Channel
- 下一步：用户需要在 ilinkai.weixin.qq.com 或企业微信 App 里找到机器人添加使用

---

*Update this file as you learn. It's how you persist.*
