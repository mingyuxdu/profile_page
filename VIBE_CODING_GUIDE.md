# Vibe Coding 方案

## 技术路线

第一阶段建议使用纯静态网站：

- 语言：HTML、CSS、JavaScript
- 编辑器：VS Code 或 Cursor
- 调试方式：浏览器开发者工具 + Live Server
- 部署方式：Cloudflare Pages / GitHub Pages / Netlify

这个路线对新手最友好：不需要数据库，不需要服务器，不需要复杂打包工具。你可以先把内容、审美和个人风格跑通，再决定是否升级到 Astro、Next.js 或带 CMS 的博客系统。

## 推荐工作流

1. 先描述目标：例如“把首页改得更像电子工程师和摄影师的混合个人主页”。
2. 让 AI 修改文件：明确说明要改 `index.html`、`styles.css` 还是全部。
3. 本地打开网页检查：看布局、文字、按钮、手机尺寸是否舒服。
4. 把不满意的地方继续用自然语言反馈：例如“项目卡片太像模板，请更克制、更专业”。
5. 每次满意后保存一个版本：推荐用 Git。

## 适合直接复制给 AI 的提示词

```text
你现在是我的个人网站前端搭档。请基于当前文件继续修改，不要重写整个项目。
目标：让这个个人主页更适合展示我的 AI 创意开发、电子实验、博客文章和摄影作品。
要求：
1. 保持纯 HTML/CSS/JS，不引入复杂框架。
2. 修改前先说明你要改哪些文件。
3. 修改后告诉我如何本地检查。
4. 保持页面适合未来绑定个人域名和面试展示。
```

## 调试器配置

### 浏览器调试

1. 用浏览器打开 `index.html`。
2. 按 `F12` 打开开发者工具。
3. 使用 `Elements` 查看 HTML 和 CSS。
4. 使用 `Console` 查看 JavaScript 报错。
5. 点击设备图标切换手机预览。

### VS Code 推荐插件

- Live Server：保存文件后自动刷新网页。
- Prettier：格式化 HTML、CSS、JavaScript。
- GitLens：查看版本变化。

### 可选 VS Code 调试配置

如果你用 VS Code，可以新建 `.vscode/launch.json`：

```json
{
  "version": "0.2.0",
  "configurations": [
    {
      "type": "msedge",
      "request": "launch",
      "name": "Open local profile page",
      "file": "${workspaceFolder}/index.html"
    }
  ]
}
```

如果你使用 Chrome，把 `type` 改成 `chrome`。

## 后续升级路线

### 阶段 1：静态名片

目标：让网站能看、能发、能用于面试。

内容包括：首页、自我介绍、项目、文章列表、摄影、联系方式。

### 阶段 2：真实内容

目标：把占位内容换成你的作品。

建议建立：

- `assets/`：头像、照片、项目封面、简历 PDF。
- `posts/`：文章草稿，可以先放 Markdown。
- `projects/`：项目资料和截图。

### 阶段 3：博客系统

当文章变多后，升级到 Astro。它适合个人博客和作品集，仍然比较轻量。

推荐技术栈：

- Astro
- Markdown / MDX
- Cloudflare Pages

### 阶段 4：自动化与 AI

可以加入：

- AI 辅助文章摘要
- 项目标签筛选
- 摄影作品瀑布流
- 中英文双语切换
- RSS 订阅
