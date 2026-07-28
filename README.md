# MMD HUD Release · dev 通道

这是 **不稳定测试通道**，由 `npm run publish:dev` 自动覆盖，随时会被推翻。
正式版本请切到 `main` 分支查看 tag 外链。

## 为什么用 commit SHA 而不是 `@dev`

jsDelivr 对分支名这类可变引用缓存 12 小时，迭代时会一直拿到旧包。
40 位 commit SHA 属于不可变引用，每次提交天然就是新 URL，既不用等缓存也不用 purge。

```html
<script src="https://cdn.jsdelivr.net/gh/Godcount10/mmd-hud-release@<commit-sha>/mmd-hud.js"></script>
```

具体 SHA 由 `publish:dev` 在推送后打印。**不要**把 `@dev` 写进任何长期使用的注入脚本。

## 产物

`manifest.json` 记录本次 dev 构建的字节数、SHA-256，以及对应的源码仓库 `sourceRef`，
用于核对 CDN 上拿到的文件与本地构建是否一致。

产物为单文件 IIFE，第三方库全部本地打包，运行时不发起任何库或字体的网络请求。
