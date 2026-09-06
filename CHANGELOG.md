# CHANGELOG —— 本仓库自身的变更记录

> 每个版本的变更见 GitHub Releases 与 git log；本文件记录关键版本的定位与影响。

## v2.0.0 · 2026-09-07 · 重新定位：跨 Agent 的个人开发上下文层

- **执行 Agent**：ZCode（GLM-5.3-Flash）
- **修改内容**：
  - 新增 3 份模板：`USER_PROFILE.md`（用户开发画像）、`WORKFLOW.md`（工作协议）、`HANDOFF.md`（交接记录），模板从 6 份变 9 份
  - `PROJECT_CONTEXT.md` 增加项目档案（目标 / 技术栈 / 当前版本 / 当前阶段）与「本地运行与验证」「环境与发布」，原「用户偏好与约定」迁出至 `USER_PROFILE.md`
  - `AGENTS.md` 重写：新的必读顺序表（PROJECT_CONTEXT → HANDOFF → USER_PROFILE → WORKFLOW → 三份按需文档），红线加入"不改架构 / 不删功能 / 不擅自部署"
  - `DECISIONS.md` / `CHANGELOG.md` / `ROADMAP.md` 保留，说明头重申职责（为什么 / 谁改的 / 往哪走）
  - `SKILL.md` 按新定位重写：核心原则从 1 条扩为 3 条（状态在文档 / 用户也是上下文 / 协议随项目走），新增「从 v1 升级」流程，开工必读加入 USER_PROFILE 与 HANDOFF，收尾增加 HANDOFF 条目与汇报四件套；v1.1.x 的部署接力 / 远端管理 / 主文件夹模型全部保留
  - `README.md` 按新定位重写：讲清"个人开发者因免费额度切换 AI 工具"的问题与解法，明确"不做多 Agent 编排"的设计边界
- **原因**：v1 只记项目状态、不记用户——换 Agent 后仍要重新培养；新定位聚焦个人开发者因额度 / 价格在多个 AI 工具间切换同一项目的真实工作流
- **影响**：初始化模板 6 → 9 份；存量 v1 项目可按 SKILL.md「从 v1 升级」平滑补齐，旧文件不删不改名
- **下一步**：找真实项目跑一轮完整换班（ZCode → 其他工具），按实测反馈迭代

## v1.x

见 [GitHub Releases](../../releases) 与 git log：

- v1.0.0：AI 项目接力框架（SKILL + 6 份治理文档模板）
- v1.1.0：远端管理询问机制 + 上传/删除解耦确认
- v1.1.1：删除确认硬门槛
- v1.1.2：项目主文件夹模型（固定项目之家 + workspace 周期性回收 + 镜像同步）
