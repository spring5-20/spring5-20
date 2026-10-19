<div align="center">

# 杨磊

**大模型智能体开发实习工程师**

LLM 应用工程 · Agent 编排 · RAG · 可观测性 · FastAPI

[![Email](https://img.shields.io/badge/Email-3407047940%40qq.com-0A66C2?style=flat-square&logo=gmail&logoColor=white)](mailto:3407047940@qq.com)
[![GitHub](https://img.shields.io/badge/GitHub-spring5--20-181717?style=flat-square&logo=github)](https://github.com/spring5-20)

</div>

## 关于我

我关注如何把大模型能力真正落到可运行、可观察、可评估的业务系统里，而不仅是停留在一次性的 Demo。

目前主要实践方向包括：

- 使用 **LangGraph** 构建有状态 Agent 工作流，处理条件路由、状态恢复、人工确认与失败重规划。
- 使用 **FastAPI + SQLAlchemy Async + Pydantic v2** 构建类型清晰、可测试的异步后端。
- 使用 **pgvector / Milvus + Reranker + SSE** 构建可追溯的企业级 RAG 问答链路。
- 通过 **MCP / A2A** 暴露与组合智能体能力，并为关键链路补充追踪、指标、日志和离线评估。

## 代表项目

### 01 · 智枢｜多智能体协作平台

面向企业多业务场景的统一 Agent 入口。由 supervisor 根据用户意图分发请求，支持天气查询、钉钉办公、电商导购、智能问数等能力，并统一处理人工确认、跨会话记忆、工具调用与可观测性。

- 交付 5 个零构建前端、59 个 API 路径与 2 个 MCP 服务。
- 以 SSE 事件契约公开 `agent_call`、`agent_result`、`confirm_required`、`done` 等过程状态。
- 接入 LangSmith、Prometheus、RAGAS 与黄金用例，覆盖质量、时延、Token 成本和工具调用准确率。

[查看项目](https://github.com/spring5-20/Multi-Agent-Orchestration-Platform) · `FastAPI` `LangGraph` `MCP` `A2A` `PostgreSQL`

### 02 · 企业知识库 RAG 问答系统

面向企业知识分散、检索低效与数据泄露风险设计的多模态 RAG 系统。覆盖文本 PDF、扫描 PDF 与图片入库，提供引用溯源、增量失效、缓存降级和人工审批。

- 跑通文档解析、语义切分、向量召回、两阶段重排、流式生成和来源引用全链路。
- 使用 `text-embedding-v4 + pgvector + qwen3-rerank + DeepSeek` 组合检索与生成能力。
- 基于 LangGraph 实现自检、问题改写与 human-in-the-loop 审批。

[查看项目](https://github.com/spring5-20/business-rag-demo) · `RAG` `LangChain` `LangGraph` `pgvector` `SSE`

### 03 · 校园报修协作系统

六人前后端团队协作项目，实现“学生报修 → 维修接单/管理员指派 → 维修完成 → 学生验收”的完整闭环。本人负责维修端与管理端后端、状态机、并发控制、定时任务和联调文档。

- 独立交付 11 个 API 路径与约 2400 行后端代码。
- 使用条件更新实现 5 状态、7 动作的并发安全状态机。
- 全项目 119 个测试用例通过，覆盖 401/403/404/409 等权限与冲突语义。

[查看项目](https://github.com/spring5-20/campus-repair-system) · `FastAPI` `MySQL` `JWT` `APScheduler` `React`

## 技术栈

| 方向 | 主要技术 |
| --- | --- |
| Agent / LLM | LangGraph、LangChain、MCP、A2A、DeepSeek、DashScope |
| 后端工程 | Python、FastAPI、Pydantic v2、SQLAlchemy 2.0 Async、JWT |
| 检索与记忆 | RAG、pgvector、Milvus、Reranker、RAGAS、Checkpointer |
| 数据与中间件 | PostgreSQL、MySQL、Redis、Alembic |
| 接口与流式 | REST、SSE、WebSocket、OpenAPI |
| 工程化 | Docker Compose、Nginx、uv、pytest、Ruff、mypy |

## 工程关注点

- **可控性**：写操作先确认，关键状态可恢复，失败可重试。
- **可追溯性**：保留路由轨迹、知识来源、工具调用和决策过程。
- **可评估性**：把正确性、时延、成本与稳定性纳入持续验证。
- **可演进性**：通过注册表、协议适配与分层设计降低新增业务线的接入成本。

---

<div align="center">

持续学习，持续构建，把复杂问题拆成可验证的工程路径。

</div>
