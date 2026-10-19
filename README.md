<div align="center">

# Serate

**空间智能体 Runtime · 3D Gaussian Splatting Web 渲染**

[个人站点](https://serate.github.io) &nbsp;·&nbsp; [技术笔记](https://serate.github.io/blog/) &nbsp;·&nbsp; [RSS](https://serate.github.io/rss.xml)

</div>

---

## 项目

### [Spatial Agent](https://github.com/Serate/spatial-agent) — 空间智能体 Runtime

把自然语言的空间问题转成结构化任务计划，经工具契约校验后驱动真实 GIS 执行，并在前端展示答案、计划、步骤轨迹、数据质量与空间结果。

- **领域路由先于执行** — `DomainSelector` 先在有界能力目录内选择、澄清，或明确说明无匹配
- **模型不直接触碰后端** — 所有工具经 schema 校验与 `ToolRegistry` 分发，工具边界因此是可控的
- **像元安全门控** — DEM 与土地利用的联合分析要求明确的网格对齐证据，证据不足时在执行前解释性阻止
- **可观测** — 中文答案、TaskPlan、执行轨迹、provenance、GeoJSON summary 与 JSON artifact 全量留存

`Python` `GeoPandas` `Rasterio` `GDAL / PROJ` `SQLite` `Docker`

### [Aholo Viewer](https://github.com/Serate/aholo-block-lod) — 3DGS & Mesh 高性能渲染器

面向超大 3D Gaussian Splatting 场景的高性能渲染器单体仓库，以 Chunked Streaming LOD 组织数据。

- **Chunked Streaming LOD** — 分块流式加载，控制超大 3DGS 场景的内存与带宽预算
- **Block + tree traversal** — 把空间索引与遍历策略解耦，定位与剔除可以分别演进
- **pnpm 单体仓库** — 渲染器 TypeScript 源码包与 Astro 文档站、示例、API 文档同处一地

`TypeScript` `C / C++` `WebGL` `Astro` `pnpm`

---

## 技术笔记

| 文章 | 时间 |
| :-- | :-- |
| [让 Agent 的 GIS 结论可被追问](https://serate.github.io/blog/evidence-chain/) | 2026.10 |
| [让模型写计划，但别让模型碰工具](https://serate.github.io/blog/agent-task-plan/) | 2026.09 |
| [3DGS 场景为什么要分块流式加载](https://serate.github.io/blog/gsplat-lod-streaming/) | 2026.08 |

---

## 在做什么

| 方向 | 说明 |
| :-- | :-- |
| **空间智能与 GIS** | 自然语言 → 任务计划 → 真实 GIS 执行。覆盖行政区边界、DEM 高程、坡度、土地利用与路网水体分析。 |
| **Agent 运行时** | 把 Planner、任务计划、工具契约、执行与恢复拆成可独立替换的层，让行为可复现、可审计、可回归。 |
| **3D 与实时渲染** | 3D Gaussian Splatting 与 Mesh 的浏览器端渲染，关注分块流式 LOD、几何与相机，以及超大场景的性能预算。 |
| **工程与交付** | 从原型到可运维服务的完整链路：容器化、CI、持久化状态，以及面向 AI 协作的仓库规范与文档。 |

---

## 站点

个人站点托管在 GitHub Pages，用 Astro 构建，无前端框架，字体全部自托管。

**在 [serate.github.io](https://serate.github.io) 看看 →**

---

<div align="center">
  <sub>武汉 · <a href="https://github.com/Serate">@Serate</a></sub>
</div>
