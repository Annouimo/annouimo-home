# Annouimo 个人主页

[annouimo.com](https://annouimo.com/) 汇集博客、书与影和精选 GitHub 项目。

- 站点介绍和精选项目写在 `content/_index.md`。
- 首页模板在 `layouts/`，样式在 `assets/css/portal.css`。
- 四站图标的 SVG 原稿在 `static/icons/`。
- [共用设计规范（初稿）](docs/design-system.md)

## 本地构建与发布

使用 Hugo 0.170.1（已验证版本）。

```sh
hugo server
hugo --minify --cleanDestinationDir
```

`wrangler.toml` 指向生产 Worker `annouimo-home`，自定义域名和 `www` 跳转由 Cloudflare 管理。构建后可用 `npx wrangler versions upload` 生成版本预览。确认预览后，再将该版本部署到生产流量。
