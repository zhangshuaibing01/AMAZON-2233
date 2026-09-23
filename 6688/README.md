# 6688 · 独立任务空间

`6688/` 是 AMAZON-2233 仓库内的独立任务线，与 `web-console/`（1122 / 2233 前端）完全解耦。

## 组成

| 文件 | 作用 |
|---|---|
| `index.html` | 站点主页，单文件静态页，内联样式，无任何外部依赖 |
| `README.md` | 本说明 |

## 线上地址

- 自定义域名：<https://6688.sorilo-uk.com>
- Pages 默认地址：<https://6688.pages.dev>

## 发布方式

推送到 `main` 且改动命中 `6688/**` 时，`.github/workflows/deploy-6688-pages.yml` 会自动把本目录部署到 Cloudflare Pages 项目 `6688`。

也可本地手动部署：

```bash
wrangler pages deploy 6688 --project-name=6688 --branch=main
```

## 约定

- 本目录内容不引用 `1122-*` / `2233-*` 的 Worker，不依赖任何后端，可独立上线。
- 后续 6688 的任务内容一律放在本目录内，不改动仓库其他板块。
