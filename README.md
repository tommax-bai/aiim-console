# aiim-console

AIIM 的**管理后台前端**（运营 Web 控制台，对应 AIDCP 的 `aidcp-console`）。

> 契约 / 设计在控制仓 [`../aiim`](../aiim)；后端 panel API 在 [`../aiim-service`](../aiim-service) 的 `apps/panel`。

## 铁律

- **只读 panel API + 经 `/api` 下发指令，绝不直连微信网关**（所有读写都经 `aiim-service/apps/panel`）。
- 类型契约来自 `aiim-service/packages/contracts` 的 panel API DTO（service ↔ console 单一真源）。

## 计划能力（随后端迭代）

- 账号总览：在线/健康度/风控状态/掉线告警、调档、暂停/恢复。
- 客户与会话：加友任务链路、对话记忆查看、送达/撤回/被删状态。
- 运营：SOP/群/朋友圈排期与执行率、高风险动作人审、运营统计漏斗。
- 告警：AI 回不上/超时、风控迁移、掉线扫码。

## 技术栈（拟）

React + Vite + TS + AntD（对齐 aidcp-console）。**骨架待初始化**。
