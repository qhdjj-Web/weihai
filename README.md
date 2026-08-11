# 🏖️ 威海景点游玩规划器

一个简单便捷的威海自助游玩路线规划网页应用，支持多人协作选择心仪景点，一键生成出行路线。

![License](https://img.shields.io/badge/License-MIT-green.svg)
![HTML5](https://img.shields.io/badge/HTML5-E34C26?style=flat&logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)

## ✨ 功能特性

- 📍 **实时地图展示** - 基于高德地图API，威海景点一览无遗
- ✅ **协作选择** - 自己和朋友可各自勾选想去的景点
- 📸 **图片管理** - 支持上传/更换景点图片，所有数据本地存储
- ➕ **动态添加** - 发现新景点？直接在应用中添加（包含图片和描述）
- 📋 **一键生成** - 将选中的景点整理成出行路线
- 💾 **数据导出** - 导出JSON文件与朋友分享景点选择
- 📂 **数据导入** - 导入朋友分享的景点数据
- 🎯 **地图联动** - 点击列表项自动定位地图，点击标记高亮列表

## 🚀 快速开始

### 在线使用
直接在浏览器中打开 `index.html` 文件即可使用，无需任何服务器配置。

```bash
# 克隆仓库
git clone https://github.com/yourusername/weihai-tour-planner.git
cd weihai-tour-planner

# 在浏览器中打开（右键 -> 用浏览器打开）
open index.html
# 或
start index.html
```

### GitHub Pages 部署
1. Fork 本仓库到你的账户
2. 在仓库设置中启用 GitHub Pages
3. 选择 `main` 分支作为发布源
4. 访问 `https://yourusername.github.io/weihai-tour-planner/`

## 📖 使用说明

### 1. 查看景点
- 左侧是威海预置景点列表，展示景点图片、时间、游玩时长等信息
- 右侧地图实时显示所有景点位置（彩色标记）

### 2. 勾选景点
- 点击景点项目的复选框勾选
- 勾选后景点会高亮显示，地图标记也会变大
- 点击列表项自动将地图定位到该景点

### 3. 更换图片
- 每个景点右侧有 "🖼️换图" 按钮
- 点击选择本地图片，图片会自动转换为 Base64 并保存
- 刷新页面后修改仍会保留

### 4. 添加新景点
- 点击 "➕ 添加地点" 按钮
- 填写：景点名称、经纬度、描述、建议时段、游玩时长、美食推荐
- 可选择上传景点图片
- 保存后新景点会出现在列表和地图上

### 5. 生成路线
- 勾选想去的景点后，点击 "📋 生成路线"
- 系统将自动整理成结构化的出行方案
- 点击 "📄 复制导出" 可复制到剪贴板，粘贴到微信/备忘录

### 6. 数据导出/导入
- **导出数据** - 将自定义景点导出为 JSON 文件
- **导入数据** - 导入朋友分享的 JSON 文件（包含图片）

## 🛠️ 技术栈

- **前端框架** - 原生 HTML5 + CSS3 + JavaScript
- **地图服务** - 高德地图 Web API v2.0
- **存储方案** - 浏览器 localStorage
- **图片处理** - File API + Base64 编码

## 📦 项目结构

```
weihai-tour-planner/
├── index.html          # 主程序（单文件应用）
├── README.md           # 项目说明文档
├── LICENSE             # MIT 开源许可证
├── .gitignore          # Git 忽略文件
├── docs/               # 文档文件夹
│   ├── FEATURES.md     # 功能详细说明
│   └── GUIDE.md        # 使用指南
└── examples/           # 示例数据
    └── sample-data.json # 示例景点数据
```

## 💾 数据存储

所有数据都存储在浏览器的 **localStorage** 中：

| 数据项 | 说明 | 容量限制 |
|------|------|--------|
| `selSpot` | 已勾选景点的索引数组 | ~5MB |
| `customSpots` | 用户添加的自定义景点 | ~5MB |
| `defaultImgOverride` | 默认景点修改后的图片 | ~5MB |

**注意**：
- 不同浏览器数据互不同步，需手动导出/导入
- 浏览器隐私模式下数据不会被保存
- 手动清除浏览器数据会导致所有数据丢失

## 🔐 隐私与安全

- ✅ 所有数据存储在本地，不上传到任何服务器
- ✅ 支持离线使用（下载 HTML 文件即可）
- ✅ 图片转换为 Base64 格式存储，不依赖外部存储
- ✅ 开源代码，完全透明

## 🤝 多人协作方案

### 方式一：导出/导入
1. 人员A勾选景点 → 导出数据得到 JSON 文件
2. 人员A将文件发给人员B
3. 人员B导入 JSON 文件 → 合并景点库
4. 人员B继续添加/修改 → 再次导出

### 方式二：屏幕共享
- 通过视频通话共享屏幕，实时讨论各景点

### 方式三：仓库协作
- Fork 本项目并修改 `index.html` 中的默认景点
- 创建分支维护不同城市的版本

## 🐛 已知限制

- 高德地图 API Key 是公开的，生产环境应替换为私有 Key
- 景点数据限制在威海地区（经度 120-124，纬度 36-38）
- 浏览器 localStorage 限制每个源约 5-10MB
- 图片以 Base64 编码存储，大图片会占用较多空间

## 🔧 自定义配置

### 修改高德地图 API Key

编辑 `index.html`，找到第 8 行：

```html
<script src="https://webapi.amap.com/maps?v=2.0&key=YOUR_API_KEY"></script>
```

替换为你的 API Key：[申请地址](https://lbs.amap.com/)

### 修改默认景点

编辑 JavaScript 中的 `spotList` 数组，修改景点信息。

### 修改地图中心和缩放级别

```javascript
map = new AMap.Map('map', {
    zoom: 10.5,           // 缩放级别
    center: [122.22, 37.49]  // 中心坐标
});
```

## 📝 License

MIT License - 详见 [LICENSE](LICENSE) 文件

## 🙌 贡献

欢迎提交 Issues 和 Pull Requests！

如果这个项目对你有帮助，不妨给个 ⭐ Star 支持一下。

## 📧 联系方式

- 提交 Issue
- Fork 后自行改进
- 在讨论区分享使用心得

---

**最后更新**: 2026年8月  
**维护者**: [Your Name]
