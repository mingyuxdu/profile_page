# 赵明宇个人主页

这是一个偏科研主页和技术工作者主页风格的静态网站，用于展示个人信息、英文简介、技术博客和摄影兴趣入口。

## 文件说明

- `index.html`：网页内容，改文字和链接主要编辑这里。
- `styles.css`：视觉样式，颜色、布局、字号、卡片都在这里。
- `about.html`：英文个人简介，包括教育、工作经历、研究方向、成果、任职和奖项。
- `electronics.html`：电子设计博客归档页。
- `photography.html`：摄影作品子页面。
- `posts/`：文章子页面。
- `script.js`：预留给未来轻量交互。
- `VIBE_CODING_GUIDE.md`：如何用 vibe coding 继续迭代。
- `DEPLOYMENT_GUIDE.md`：上线和绑定个人域名的方法。

## 本地查看

直接双击 `index.html` 即可在浏览器打开。

如果以后你使用 VS Code，也可以安装 Live Server 插件，然后右键 `index.html` 选择 `Open with Live Server`。

如果你想用本地服务器预览，可以在当前文件夹运行：

```bash
node preview-server.js
```

然后访问：

```text
http://localhost:5500/
```

## 推荐下一步

1. 把首页中的邮箱、研究方向和个人照片替换为真实信息。
2. 把 `about.html` 中的英文占位履历替换为真实履历。
3. 在 `posts/` 中继续新增文章页面，并同步更新 `index.html` 和 `electronics.html`。
4. 上传到 GitHub，并用 Cloudflare Pages 或 GitHub Pages 部署。
