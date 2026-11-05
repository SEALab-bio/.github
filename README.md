<p align="center">
  <img src="https://raw.githubusercontent.com/SEALab-bio/.github/main/assets/logo.webp"
       alt="SEA Lab" width="150" />
</p>

# SEALab-bio · `.github`

本仓库是 **SEA Lab**（`SEALab-bio`）组织的配置仓库。

组织主页（<https://github.com/SEALab-bio>）上显示的内容在 [`profile/README.md`](profile/README.md)，
**不是**本文件。

## 目录结构

| 路径 | 作用 |
|---|---|
| `profile/README.md` | 组织主页内容，渲染在 org 的 Overview 标签 |
| `README.md` | 本文件，仅显示在本仓库页面 |
| `assets/` | 视觉素材：`logo` / `hero` / `mascot`，均有 `.png` 源图与 `.webp` 网页版 |
| `.github/workflows/snake.yml` | 贡献贪吃蛇，每日 UTC 0 点生成 SVG 并推送到 `output` 分支 |

## 三个容易踩的坑

1. **workflow 必须在 `.github/workflows/`**，放根目录 `workflows/` 不会被 GitHub 识别。
2. **org profile README 必须在 `profile/README.md`**，放根目录不会显示在组织主页。
3. **profile README 里引用图片要用绝对地址**（`raw.githubusercontent.com/...`）。
   组织主页的 base URL 是 `/SEALab-bio`，相对路径 `assets/xxx.webp` 会解析成
   `github.com/SEALab-bio/assets/...` 从而 404。

## 素材说明

`assets/` 下每个素材都保留 `.png` 源图与压缩后的 `.webp` 网页版，README 只引用 `.webp`：

| 素材 | 源图 | 网页版 | 用途 |
|---|---|---|---|
| `logo` | 1412KB | 45KB | 组织头像 / 本页顶部 |
| `hero` | 2165KB | 259KB | 组织主页顶部横幅 |
| `mascot` | 1794KB | 137KB | 组织主页收尾暖场 |

如需更新素材，替换 `.png` 源图后用 Pillow 重新导出 `.webp`（quality 88）即可。
