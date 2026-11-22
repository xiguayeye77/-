# SHIQI · 王仕祺的个人站

线上地址：https://xiguayeye.icu

一个以梵高《星空》为视觉基调的个人站。没有框架、没有构建步骤，用原生 HTML / CSS / JavaScript 写成，打开就能跑。

## 关于

我是王仕祺（SHIQI），AI 开发学习者，喜欢 3D 打印、无人机、摄影和台球。这个站点用来记录做过的东西：项目、游戏、常用网站，还有一些折腾过程。

## 功能

- 首页姓名使用 Depth Text：同一句话叠 34 层，沿 Z 轴挤出厚度，鼠标移动时整体倾斜
- 介绍文字使用 Warp Text：悬停时文字沿波浪形变
- 背景由梵高星空底图与幽灵纤维（WebGL）画布叠加而成
- 项目按 3D 打印、无人机、摄影、软件开发、产品开发、台球分类筛选
- 项目与游戏均为单列布局，标题带可变邻近度效果
- 网页区一行 7 个图标入口
- 文章管理：密码解锁后可发布 / 删除文章，数据保存在浏览器 localStorage
- 响应式布局，支持 `prefers-reduced-motion`

## 技术栈

- HTML5 + CSS3（自定义属性、Grid / Flex、`backdrop-filter`）
- 原生 JavaScript（IntersectionObserver、requestAnimationFrame、Canvas）
- WebGL 着色器（幽灵纤维背景）
- 字体：文章页使用本地 JetBrains Mono 与 Instrument Serif

## 目录结构

```text
.
├── index.html              首页
├── css/style.css           全站样式
├── js/main.js              交互、文章数据、文字与背景效果
├── assets/                 头像与星空底图
└── creation-story/         建站过程长文（自包含页面）
```

## 本地运行

```bash
python -m http.server 4173
```

然后打开 http://127.0.0.1:4173

## 部署

托管在 Cloudflare Pages，项目名 `shiqisite`，绑定域名 `xiguayeye.icu`。

```bash
wrangler pages deploy . --project-name shiqisite --branch main
```

## 相关文章

《从一张星空图到上线：我的个人站搭建全记录》——记录视觉、背景、文字效果、列表改造和部署踩坑的完整过程。

在线阅读：https://xiguayeye.icu/creation-story/creation-story.html

## 联系

- 邮箱：932652826@qq.com
