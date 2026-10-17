# Third-party notices

## 第三方来源与许可证

本包的 `vendor/official-client.cjs` 是官方 npm 包
`@deepseek-ai/dsh-client-ui-settings-models` 的**客户端产物原样副本**（DSH 核心 `0.2.0-rc.2` 随附版本）。
`scripts/build-fork.mjs` 在这份副本上打补丁生成 `dist/client.cjs`，只新增「思考模式」相关的控件；
页面 id、侧边栏位置、顺序与文案均与官方一致。本包不是上游官方发布或背书的插件。

- 许可证：MIT。
- 原始版权声明：`Copyright (c) 2026 DeepSeek`。
- 上游仓库：https://github.com/deepseek-ai/deepseek-harness ，对应目录
  `packages/client/ui-settings-models`。
- 本包 `LICENSE` 取自同一上游 MIT 声明，未改写版权人或年份。
- 核验日期：2026-10-17。`vendor/official-client.cjs` 与 `dist/client.cjs` 的差异**仅有**下列补丁，
  每个补丁在 `scripts/build-fork.mjs` 中都断言「命中且仅命中一次」——对更新版本重新 fork 时会显式失败，
  而不是静默产出一份被改花的页面。

React 与 DSH 宿主服务由宿主提供，不是本包随附的另一套运行时，各自的许可证仍适用。
此声明不将本地修改冒充上游作品，也不虚构本地修改的版权归属。
