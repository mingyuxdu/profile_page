# 上线与绑定个人域名

## 推荐方案：GitHub + Cloudflare Pages

这套方案适合新手，免费额度充足，绑定域名也清晰。

## 步骤 1：准备 GitHub 仓库

1. 注册或登录 GitHub。
2. 新建仓库，例如 `profile_page`。
3. 把当前文件夹上传到仓库。

如果以后会用命令行，可以在本地运行：

```bash
git init
git add .
git commit -m "Initial personal profile site"
git branch -M main
git remote add origin https://github.com/你的用户名/profile_page.git
git push -u origin main
```

## 步骤 2：部署到 Cloudflare Pages

1. 打开 Cloudflare Dashboard。
2. 进入 `Workers & Pages`。
3. 选择 `Create application`。
4. 选择 `Pages`，连接 GitHub 仓库。
5. 构建设置：
   - Framework preset：None
   - Build command：留空
   - Build output directory：`/`
6. 点击部署。

部署完成后，你会得到一个临时域名，例如：

```text
https://profile-page.pages.dev
```

## 步骤 3：购买个人域名

你可以在这些平台购买域名：

- Cloudflare Registrar
- Namecheap
- 阿里云
- 腾讯云

建议选择简短、好记、适合长期使用的域名，例如：

```text
yourname.com
yourname.dev
yourname.cn
```

## 步骤 4：绑定个人域名

如果域名也在 Cloudflare 管理：

1. 在 Cloudflare Pages 项目里进入 `Custom domains`。
2. 添加你的域名，例如 `www.yourname.com`。
3. 按提示确认 DNS 记录。
4. 等待 SSL 证书自动生效。

如果域名不在 Cloudflare 管理：

1. 在域名服务商后台找到 DNS 设置。
2. 添加 `CNAME` 记录：

```text
主机记录：www
记录类型：CNAME
记录值：你的 pages.dev 域名
```

3. 回到 Cloudflare Pages 添加 `www.yourname.com`。

## 根域名与 www

建议同时支持：

```text
yourname.com
www.yourname.com
```

常见做法：

- `www` 使用 CNAME 指向 Cloudflare Pages。
- 根域名使用 Cloudflare 的 CNAME flattening 或按平台提示配置。

## 上线后的日常更新

以后你只需要：

1. 修改本地文件。
2. 提交到 GitHub。
3. Cloudflare Pages 会自动重新部署。

如果你暂时不会 Git，可以先用 GitHub 网页上传文件，等熟悉后再学习命令行。
