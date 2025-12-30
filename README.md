# Melbourne Trip Guide

> 一个基于静态 HTML 的墨尔本旅游指南示例项目 — 轻量、可直接部署到 GitHub Pages 供演示与教学使用。

[![Languages](https://img.shields.io/github/languages/top/JYZ-LESLIE/melbourne-trip-guide?color=blue&label=Languages)](https://github.com/JYZ-LESLIE/melbourne-trip-guide)
[Demo（GitHub Pages）](https://JYZ-LESLIE.github.io/melbourne-trip-guide/)（如果未启用 Pages，请参见下方“运行 & 发布”）

TL;DR
- 这是一个静态网站仓库；代码语言构成为：HTML — 100%。
- 适合快速预览（直接打开 index.html）或部署到 GitHub Pages 做演示。
- README 包含快速预览、运行方法、文件结构与贡献指南，便于他人复用。

项目概述（1 行）
- 目标：以静态页面形式展示墨尔本旅游要点（景点、路线、交通与小贴士），适合教学与演示使用。

主要亮点
- 纯静态：无需后端或构建流程，直接托管于 GitHub Pages。  
- 结构清晰：单页面/多页面布局均可快速修改与扩展。  
- 易于复用：把 index.html 拷贝到其他 repo 即可作为演示页。

技术栈
- HTML: 100%（项目所有源文件为静态 HTML、图片与静态资源）
- 建议：后续若加入 CSS/JS，可在 README 中更新语言占比与演示截图。

如何本地预览
1. 克隆仓库：
   git clone https://github.com/JYZ-LESLIE/melbourne-trip-guide.git
2. 快速预览（最简单）：
   - 在文件管理器中打开 `index.html`，或用浏览器打开本地文件路径。
3. 推荐（使用本地静态服务器，避免部分浏览器安全限制）：
   - 使用 Python3：`python -m http.server 8000`，然后访问 `http://localhost:8000`

如何部署到 GitHub Pages（快速）
1. Settings > Pages 中将 Source 设为 `main` 分支的 `/ (root)` 或 `gh-pages` 分支。  
2. 将构建文件（index.html 等）推送到对应分支，等待几分钟即可访问：  
   https://<用户名>.github.io/<仓库名>/  
   示例： https://JYZ-LESLIE.github.io/melbourne-trip-guide/

推荐的仓库结构（示例）
- index.html            # 主页（必读）
- assets/css/           # 样式
- assets/img/           # 截图/图片（建议放封面 cover.png）
- assets/js/            # 脚本（如有）
- README.md             # 项目说明（当前文件）
- language-bar.html     # （可选）语言占比可视化条

如何提升仓库展示（优先级）
1. 在 README 顶部放一张 900×400 的封面截图（/assets/img/cover.png）以吸引访客。  
2. 启用并展示 GitHub Pages Demo 链接。  
3. 使用 Shields Badge（语言、License、Pages 状态、最近提交）提高可信度。  
4. 在 README 增加“如何复用/移植”示例（如复制 index.html 并改图）。  
5. 若加入 CSS/JS，请在 README 更新语言占比图表或 language-bar.html。

贡献
- 欢迎提交 issue 或 PR。建议在 PR 描述中附上截图或 GIF 以帮助审阅。

许可证
- 如果你愿意，建议添加 LICENSE（例如 MIT）。

作者与联系方式
- JYZ-LESLIE（仓库所有者）
