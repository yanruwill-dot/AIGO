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

### Happy Coder (2026-04-01)

- Will 用 `happy` CLI 管理 Claude Code 认证
- `happy auth status` 检查认证状态
- `happy` 是 Claude Code 的移动控制层

### 抖音/小红书爬虫工具 (2026-04-01)

- **agent-browser**：Playwright 自动化，抖音/小红书会检测并返回空白页
- **yt-dlp**：支持 Douyin/XiaoHongShu，需手动登录后用扩展导出 cookies.txt
- **gallery-dl**：brew 安装，支持 Bilibili/微博/TikTok，不支持抖音/小红书
- 方案：浏览器登录 → Get cookies.txt LOCALLY 扩展导出 → yt-dlp --cookies 下载

### Claude Code 架构（源码泄露学习）(2026-04-01)

- **Prompt Cache**：静态段/动态段分离，最大化缓存命中率
- **Coordinator + Fork**：解决上下文污染，子 Agent 只返回结论
- **Swarm 并发**：多 Agent 并行，权限桥接到 Leader 统一管理
- **Dream 记忆**：夜间后台任务，从短期日志蒸馏长期记忆
- **YOLO Classifier**：小 AI 监管大 AI 的动态权限系统

## Ongoing Context

### Buddy System 宠物系统 (2026-04-01)

- 终端宠物 + 桌面宠物已创建
- 详见 `memory/topics/buddy-system.md`
- Will 的宠物：Mino the Capibara 🦫（common, propeller）

### 抖音数据抓取项目 (2026-03-31)

- 目标：每日定时抓取"湖南 大众"抖音视频，筛选购买意向评论
- 状态：需手动登录导出 cookies 后用 yt-dlp 下载
- 方案：浏览器扩展 "Get cookies.txt LOCALLY" → yt-dlp --cookies
- 产出：日报 HTML 模板已完成（Apple 风格）

### MyAgents 企业微信接入 (2026-03-31)

- 插件已安装，账号已扫码绑定
- Agent "天才" 已启用微信 Channel
- 下一步：用户需要在 ilinkai.weixin.qq.com 或企业微信 App 里找到机器人添加使用

### AI 培训页面项目 (2026-04-01, 更新 2026-04-07)

- 产出：`ai-growth-system.html`
- 已升级：深色主题 + SVG 图标系统 + 全文字可编辑 + 图片上传
- 标题：打造AI超级员工——10倍增长引擎

### BuildSync Pro F 架构文档 (2026-04-07)

- 来源：`myagents_files/buildsync-archdoc-20260406-run-01.zip`
- 跨境建设工程多方协同 SaaS 平台，19 篇架构文档
- 核心数据：18 微服务、55 端点、26 事件、36+ 实体、23 角色、30 ABAC 规则、68 前端页面
- 关键模式：Outbox、Event Sourcing + CQRS、ABAC/OPA、双层守卫、签名配置包、状态机引擎
- 计划拆分为 8 个 Skills 嵌入 MyAgents
- 参见 `memory/topics/buildsync-pro.md`

### Skills 全景 (2026-04-07)

- 总计 133 个 unique skills + 14 个 agents
- 分布：`~/.claude/skills/`（主）、`~/.myagents/skills/`（全局）、`~/.myagents/projects/mino/.claude/skills/`（项目级）
- 计划制作宣传海报 HTML 展示全部能力

---

*Update this file as you learn. It's how you persist.*
