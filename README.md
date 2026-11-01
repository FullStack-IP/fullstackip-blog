# Fullstack 全栈社博客

全栈社的技术博客，记录全栈开发相关的文章与心得。

<https://fullstackip.dpdns.org/>

基于 **Astro 6** + **Svelte 5** 构建，使用开源主题 [Firefly](https://github.com/CuteLeaf/Firefly)。

## 技术栈

- Astro 6 / Svelte 5 / TypeScript
- Tailwind CSS 4
- Pagefind 全文搜索
- Swup 页面过渡

## 本地运行

需要 Node.js >= 22、pnpm >= 9。

```bash
pnpm install
pnpm dev       # http://localhost:4321
```

## 常用命令

| 命令 | 说明 |
| --- | --- |
| `pnpm dev` | 启动开发服务器 |
| `pnpm build` | 生产构建，输出到 `dist/` |
| `pnpm preview` | 预览构建结果 |
| `pnpm check` | Astro 类型检查 |
| `pnpm lint` | Biome 检查并修复 |
| `pnpm format` | Biome 格式化 |
| `pnpm new-post <filename>` | 新建文章 |

## 写文章

文章位于 `src/content/posts/`，支持 Markdown 与 MDX。推荐用脚手架创建：

```bash
pnpm new-post hello-world
```

## 配置

站点信息集中在 `src/config/`：

- `siteConfig.ts` — 站点标题、域名、主题色、页面开关
- `profileConfig.ts` — 头像、昵称、社交链接
- `navBarConfig.ts` — 导航栏
- `backgroundWallpaper.ts` — 壁纸与横幅
- `commentConfig.ts` — 评论系统

部署前请把 `siteConfig.ts` 中的 `site_url` 改成实际域名。

## 部署

构建产物为纯静态文件，可部署到 Vercel、Cloudflare Workers 或 GitHub Pages。仓库内已包含对应配置：

- `vercel.json`
- `wrangler.jsonc`
- `.github/workflows/deploy.yml`

## 致谢

本项目基于 [CuteLeaf/Firefly](https://github.com/CuteLeaf/Firefly) 二次开发，Firefly 又基于 [saicaca/fuwari](https://github.com/saicaca/fuwari)。

感谢原作者与所有贡献者的开源工作。Firefly 的文档、预览与源码：

- 源码：<https://github.com/CuteLeaf/Firefly>
- 文档：<https://docs-firefly.cuteleaf.cn/>
- 预览：<https://firefly.cuteleaf.cn/>

## 许可证

[MIT](./LICENSE)。原始版权归 saicaca 与 CuteLeaf 所有。
