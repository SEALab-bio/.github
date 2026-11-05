# SEALab-bio · `.github`

本仓库是 **SEALab-bio** 组织的配置仓库。

组织主页（<https://github.com/SEALab-bio>）上显示的内容在 [`profile/README.md`](profile/README.md)，
**不是**本文件——GitHub 只从 `profile/` 目录渲染组织 Overview。

## 目录结构

| 路径 | 作用 |
|---|---|
| `profile/README.md` | 组织主页内容，渲染在 org 的 Overview 标签 |
| `README.md` | 本文件，仅显示在本仓库页面 |
| `.github/workflows/snake.yml` | 贡献贪吃蛇，每日 UTC 0 点生成 SVG 并推送到 `output` 分支 |

## 两个容易踩的坑

1. **workflow 必须在 `.github/workflows/`**，放根目录 `workflows/` 不会被 GitHub 识别。
2. **org profile README 必须在 `profile/README.md`**，放根目录不会显示在组织主页。
