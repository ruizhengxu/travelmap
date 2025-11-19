# 🗺️ 大西北深度游交互地图 (Northwest China Travel Map)

> 一个基于 Leaflet.js 的轻量级、交互式旅行规划与记录地图。
> 专为移动端优化，支持相册浏览、大图查看及深度攻略链接。

![Project Status](https://img.shields.io/badge/Status-Active-success)
![Tech Stack](https://img.shields.io/badge/Tech-HTML5%20%7C%20Leaflet.js-blue)

## 🔗 在线预览 (Live Demo)

**[👉 点击这里查看我的旅行地图](https://你的用户名.github.io/你的仓库名/)**

*(请将上面的链接替换为你开启 GitHub Pages 后的实际链接)*

---

## ✨ 功能特性

* **📍 交互式地图标记**：清晰的地图锚点，配有高可读性的地名标签。
* **📱 移动端完美适配**：禁用缩放误触，UI 自动适应手机屏幕，体验如同原生 App。
* **📝 个人笔记 & 深度攻略**：
    * 黄色高亮区域展示个人独家笔记（避坑、心得）。
    * 灰色区域展示官方或百科级的详细介绍及 Tag 标签。
* **📸 沉浸式相册**：
    * 每个地点支持多张照片轮播。
    * **灯箱模式 (Lightbox)**：点击图片即可全屏查看高清大图。
* **🔗 外部链接跳转**：内置蓝色按钮，一键跳转 Trip.com 或其他攻略网站查看详情。
* **🚀 纯静态部署**：无需后台服务器，直接托管于 GitHub Pages，永久免费。

---

## 🛠️ 如何管理与更新

本项目是一个单文件 HTML 项目，数据存储在 `index.html` 内部的 JSON 数组中。

### 1. 添加/修改地点数据

打开 `index.html`，搜索 `var locations = [`，你会看到如下结构：

```javascript
{
    name: "地点名称",
    coords: [纬度, 经度], // 使用百度地图或Google地图拾取坐标
    myNotes: ["笔记1", "笔记2"], // 你的个人笔记
    desc: "这里写详细的介绍...", // 支持 HTML 标签，如 <strong>加粗</strong>
    tags: ["标签1", "标签2"],
    link: "[https://hk.trip.com/](https://hk.trip.com/)...", // 跳转按钮的链接
    photos: [
        "photos/image_01.jpg", // 本地图片路径
        "[https://example.com/image.jpg](https://example.com/image.jpg)" // 或网络图片链接
    ]
},
