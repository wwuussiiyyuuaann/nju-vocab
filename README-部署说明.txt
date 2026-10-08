南大通用英语词汇 · 手机版（PWA）部署说明
==========================================

这个文件夹里一共 6 个文件，全部是静态文件，不需要服务器、不需要数据库：

  index.html            应用本体（词表数据已内嵌，单文件自包含）
  manifest.json         应用信息（名称、图标、全屏模式）
  sw.js                 Service Worker，负责离线缓存
  apple-touch-icon.png  iPhone 主屏幕图标（180×180）
  icon-192.png          Android / 通用图标
  icon-512.png          高清图标（同时用作 maskable）

【放到网上，得到网址】
方式 A：Cloudflare Pages —— 注册后进入 Workers & Pages → Create → Pages → Upload assets，
        把本文件夹里的 6 个文件一起拖进去，几十秒后得到一个 https://xxx.pages.dev 网址。
方式 B：GitHub —— 新建仓库（建议 Private），把这 6 个文件上传；
        再到 Settings → Pages → Source 选 main 分支根目录，保存，等 1 分钟得到
        https://<用户名>.github.io/<仓库名>/ 网址。
方式 C：Netlify Drop —— 打开 app.netlify.com/drop，把整个文件夹拖进去，立刻得到网址。

【在 iPhone 上安装】
1) 用 Safari 打开上面的网址（必须是 Safari，微信内置浏览器不行）；
2) 点底部「分享」按钮 → 往下找到「添加到主屏幕」→ 添加；
3) 主屏幕出现「南大词汇」图标，点开即是全屏应用，且断网也能用。

【注意事项】
· 学习进度（收藏、复习阶段）保存在你这台手机的浏览器里，不上传任何服务器。
  换手机、清理 Safari 数据会丢失，建议偶尔用应用内「导出 JSON 备份」存一份。
· iPhone 上如果长时间不打开，系统可能清理网站数据；添加到主屏幕后一般不会被清，
  但仍建议定期导出备份。
· 部署到公开网址时请注意：词表内容版权归南京大学，仓库建议设为私有。
