# 24节气 PWA

极简的 Progressive Web App，提供实时节气查询、倒计时和应节古诗词。

## 功能特点

- 📅 **实时节气**：自动识别当前所在的节气
- ⏰ **倒计时**：显示距离下一个节气的天数
- 📜 **应节诗词**：根据节气推送相关古诗词
- 📱 **PWA**：可安装到桌面，支持离线使用
- ⚡ **极简设计**：白底大字，移动端优化

## 快速开始

### 1. 准备图标

打开 `generate-icons.html` 在浏览器中生成所有尺寸的图标，保存到 `icons/` 目录：

```bash
# 在浏览器中打开
open generate-icons.html
```

需要以下尺寸的图标：
- 72x72, 96x96, 128x128, 144x144, 152x152, 180x180, 192x192, 384x384, 512x512

### 2. 本地预览

使用任意 HTTP 服务器预览：

```bash
# 使用 Python
python -m http.server 8000

# 使用 Node.js http-server
npx http-server

# 或使用 VS Code Live Server 插件
```

然后在浏览器访问 `http://localhost:8000`

### 3. 部署到 GitHub Pages

将项目推送到 GitHub 仓库：

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/你的用户名/solar-terms-pwa.git
git push -u origin main
```

在 GitHub 仓库设置中：
1. Settings → Pages
2. Source 选择 "GitHub Actions"

## 项目结构

```
solar-terms-pwa/
├── index.html              # 主应用（包含所有逻辑）
├── manifest.webmanifest    # PWA 配置
├── sw.js                   # Service Worker（离线支持）
├── generate-icons.html     # 图标生成工具
├── icons/                  # 图标目录（需手动生成）
└── .github/
    └── workflows/
        └── deploy.yml      # 自动部署配置
```

## 技术栈

- 纯 HTML5 + CSS3 + Vanilla JavaScript
- Service Worker API（离线缓存）
- Web App Manifest（PWA 配置）
- GitHub Actions（自动部署）

## PWA 特性

✅ **可安装**：可添加到手机桌面
✅ **离线可用**：Service Worker 缓存核心资源
✅ **响应式**：完美适配移动端
✅ **极简轻量**：单文件架构，加载快速

## 验证 PWA

在 Chrome DevTools 中验证：

1. **Application 标签**：
   - Manifest 检查
   - Service Worker 状态
   - 缓存存储

2. **Lighthouse 审计**：
   - PWA 分数应 ≥ 90
   - 性能分数应 ≥ 90

3. **PWABuilder 打包**：
   - 访问 https://pwabuilder.com
   - 输入你的 GitHub Pages URL
   - 生成 Android APK

## 数据说明

节气数据基于2026年农历计算，包含24个节气的：
- 准确日期
- 应节古诗词
- 诗词出处

## 许可证

MIT
