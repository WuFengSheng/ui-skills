# wufengsheng/skills

个人 AI Agent 技能注册表，由 [skillpod](https://github.com/anthropics/skillpod) 管理。收录 Vue 生态 UI 组件库的官方文档技能，为 Claude Code 等 AI 编程助手提供精准的组件 API 参考。

---

## 安装

```bash
# 安装单个技能
openclaw skills install @wufengsheng/<skill-name>

# 安装全部技能
openclaw skills install @wufengsheng/element-ui-vue2
openclaw skills install @wufengsheng/element-plus-ui-vue3
openclaw skills install @wufengsheng/uview-ui
```

---

## 技能列表

### element-ui-vue2

> Element UI — 基于 Vue 2.x 的饿了么桌面端组件库

| 属性 | 值 |
|------|-----|
| 框架 | Vue 2.x Options API |
| 前缀 | `el-` |
| 文档来源 | [element.eleme.cn](https://element.eleme.cn/#/zh-CN) |
| 组件数 | 69 个（+ 8 篇指南） |
| 大小 | ~1.9 MB |

```bash
openclaw skills install @wufengsheng/element-ui-vue2
```

触发场景：开发 Vue 2.x 桌面端页面、使用 `el-button`/`el-form`/`el-table` 等组件、需要组件 API 属性/事件/插槽参考。

---

### element-plus-ui-vue3

> Element Plus — 基于 Vue 3.x 的桌面端组件库，Element UI 的官方升级版

| 属性 | 值 |
|------|-----|
| 框架 | Vue 3.x Composition API（`<script setup>`） |
| 前缀 | `el-` |
| 文档来源 | [element-plus.org](https://element-plus.org/zh-CN/) |
| 组件数 | 100 个（+ 18 篇指南） |
| 大小 | ~6.0 MB |

```bash
openclaw skills install @wufengsheng/element-plus-ui-vue3
```

相比 Element UI 新增：`text`、`scrollbar`、`space`、`splitter`、`autocomplete`、`input-tag`、`mention`、`select-v2`、`table-v2`、`tree-v2`、`tour`、`segmented`、`affix`、`anchor`、`watermark` 等 30+ 组件，以及暗黑模式、SSR、自定义命名空间等指南。

触发场景：开发 Vue 3.x 桌面端页面、使用 Composition API 风格、需要暗黑模式/SSR/主题配置。

---

### uview-ui

> uView UI — 全面兼容 nvue 的 uni-app 生态框架

| 属性 | 值 |
|------|-----|
| 框架 | uni-app Vue 2.x Options API |
| 前缀 | `u-` |
| 文档来源 | [uviewui.com](https://www.uviewui.com/) |
| 组件数 | 86 个组件 + 17 个 JS 工具（+ 19 篇指南） |
| 大小 | ~1.7 MB |

```bash
openclaw skills install @wufengsheng/uview-ui
```

涵盖基础组件（16）、表单组件（16）、数据展示（17）、反馈组件（12）、导航组件（5）以及 HTTP 请求、节流防抖、时间格式化、路由跳转等 17 个 JS 工具函数。

触发场景：开发 uni-app 页面、使用 `u-button`/`u-form`/`u-modal` 等组件、需要多平台（微信/支付宝/百度/头条小程序 + H5 + App）兼容的移动端 UI。

---

## 技能设计理念

每个技能遵循相同的设计模式（由 [uview-pro](https://github.com/anthropics/skillpod) 启发）：

```
skill-name/
├── SKILL.md          # 索引锚点：触发条件 + 分类表格 + Vue 代码示例
├── llms-full.txt     # 全量文档聚合，适合大上下文单次加载
└── references/       # 独立 .md 文件，按官方分类组织，含 YAML frontmatter
```

- **内容 100% 源自官方文档**：无摘要、无改写，保证 API 准确性
- **触发条件明确**：检测到 `el-`/`u-` 组件前缀或 Vue 开发场景时自动激活
- **按需加载**：先读 SKILL.md 定位，再读对应 references/ 文档，避免上下文浪费

---

## 更新日志

| 日期 | 变更 |
|------|------|
| 2026-06-24 | 初始发布：element-ui-vue2、element-plus-ui-vue3、uview-ui |
