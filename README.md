# alpha-build

Alpha 公开打包仓。只消费版本锁（`xunchahaha/alpha` 内
`components/alpha-components.json`）指定的正式私有成品，不 checkout、
不编译私有源码。

- 首轮验证：`pull-private-check`（Actions 页手动 Run workflow）。
  用 `ALPHA_PRIVATE_PULL` 只读密钥确认三个私有仓
 （`alpha-wcdb` / `alpha-xkey` / `alpha-wxproto`）的 release 与锁 commit 可达。
- 完整组装 workflow 等私有组件首个 qualified release 发布、
  版本锁 `state` 翻为 `published` 后再搬入。
