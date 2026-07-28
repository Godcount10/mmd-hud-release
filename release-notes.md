## [0.1.0] - 2026-07-28

首个稳定版本。当前 Bridge 已足以作为 MMD 游戏 HUD 的开发基础；尚未对齐的动作会通过 Capability 明确保持不可用。

### 已实现

- MMD 原生消息、角色名称和流式生成状态镜像。
- 发送、复制、重新生成、编辑、回溯和开启新故事。
- 评论、分享、收藏和刷新对话。
- 模型分类、模型选择和动态模型设置。
- 历史会话切换与创建。
- 用户人设模式、称呼、性别和身份设置。
- 设定补充及原生位置 Picker。
- Shadow DOM 隔离的 Vue 3 HUD Runtime。
- Prototype Bridge 调试主题和开发 Mock。
- 单文件 IIFE 与可直接粘贴的 `<script>` 构建产物。

### 已知限制

- 仅适配当前已经验证的 MMD DOM 结构。
- 停止/继续生成、删除消息和分支切换等协议动作尚未实现。
- 当前默认 Theme 是 Bridge 调试台，不是最终游戏界面。
- 所有新增 Bridge 能力仍需在真实 MMD 页面回归。

[0.1.0]: https://github.com/Godcount10/mmd-hud/releases/tag/v0.1.0
