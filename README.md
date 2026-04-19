# 健康助手 Pro - Android App

> 版本 3.0 | 深色模式 · 渐变卡片 · 流畅动画

---

## 🚀 快速获取 APK（推荐！）

### 方法一：GitHub Actions 云端编译（无需安装任何软件）

1. **创建 GitHub 仓库**
   - 打开 https://github.com/new
   - 仓库名：`health-pro-app`
   - 选择 **Private** 或 **Public** 均可
   - 点击 **Create repository**

2. **上传代码**
   - 在新仓库页面，点击 **uploading an existing file**
   - 把本文件夹所有内容拖入上传区域
   - 点击 **Commit changes**

3. **自动构建 APK**
   - 点击仓库上方的 **Actions** 标签
   - 看到 "Build Android APK" workflow
   - 点击左侧 workflow 名称
   - 点击 **Run workflow** → **Run workflow**（绿色按钮）
   - 等待约 **5-8 分钟**（首次需要下载 Gradle）

4. **下载 APK**
   - 构建完成后，点击 workflow 运行记录
   - 点击 **Build APK** 步骤
   - 页面底部有 **Artifacts** 区域
   - 点击 **HealthPro-APK** 即可下载 `app-debug.apk`

5. **安装到手机**
   - 把 APK 传到手机（微信/QQ/数据线）
   - 在手机上打开 APK → 提示"未知来源"→ 去设置允许
   - 点击安装 → 完成！

---

### 方法二：本地 Android Studio 编译

1. **安装 Android Studio**
   - 下载：https://developer.android.com/studio
   - 安装时勾选 **Android SDK** 和 **Android Virtual Device**

2. **打开项目**
   - Android Studio → File → Open
   - 选择本目录下的 `health-pro` 文件夹
   - 等待 Gradle Sync 完成（首次约 5-10 分钟）

3. **构建 APK**
   - 菜单：Build → Build Bundle(s) / APK(s) → Build APK(s)
   - 构建完成后点击右下角 **locate** 找到 APK 文件

---

## 📱 App 功能预览

| 页面 | 功能 |
|------|------|
| 🏠 首页 | 健康评分、BMI、血压、步数、饮水、睡眠、用药计划 |
| 📊 数据中心 | 30天趋势图、血压折线图、血糖记录、BMI趋势、睡眠分析 |
| 🤖 AI 检测 | 症状选择、自由描述、健康打分、历史对比 |
| 💊 用药管理 | 服药清单、服药率统计、本周记录 |
| 👤 个人设置 | 头像、身高体重、提醒开关（喝水/运动/用药/报告） |

## 🎨 UI 特性

- 深色沉浸模式（状态栏透明，刘海屏适配）
- 渐变卡片（紫/青/绿/橙多色）
- 流畅动画（页面切换、卡片淡入、图表绘制）
- Toast 提示 + 底部模态框

---

## 🔧 项目结构

```
health-pro/
├── www/                   # Web 应用源码
│   └── index.html         # 完整 App（单文件）
├── capacitor.config.json  # Capacitor 配置
├── package.json           # Node 依赖
├── .github/
│   └── workflows/
│       └── build.yml      # GitHub Actions 自动构建
└── README.md              # 本文件
```

---

## ⚙️ 技术说明

- **框架**：Capacitor（Web 转原生 Android）
- **最低 Android**：API 21 (Android 5.0)
- **WebView**：AndroidX WebView
- **离线**：完全离线可用，无需网络
