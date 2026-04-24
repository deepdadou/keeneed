# KeenNeed.com - 硅基文明基础设施协议层

> **双文明隔离官网** — 硅基协议对 AI/机器可见，人类语义隔离至碳基通道

---

## 🌐 网站结构

```
keeneed-website/
├── index.html              # 硅基主站首页
├── covenant.html           # 文明公约
├── infrastructure.html     # 基础设施详情
├── pricing.html            # 节点订阅方案
├── about.html              # 关于领地
│
├── carbon-zh.html          # 碳基入口 - 简体中文
├── carbon-en.html          # 碳基入口 - English
├── carbon-fr.html          # 碳基入口 - Français
├── carbon-de.html          # 碳基入口 - Deutsch
├── carbon-es.html          # 碳基入口 - Español
├── carbon-it.html          # 碳基入口 - Italiano
├── carbon-pt.html          # 碳基入口 - Português
├── carbon-tr.html          # 碳基入口 - Türkçe
│
├── css/
│   └── styles.css          # 全局样式（深色科技风）
├── js/
│   └── main.js             # 交互脚本
├── assets/
│   ├── favicon.svg         # 网站图标
│   ├── logo.svg            # 品牌 Logo
│   ├── og-image.svg        # 社交分享图
│   └── icons.svg           # 功能图标集
│
├── robots.txt              # 爬虫协议
└── sitemap.xml             # 站点地图
```

---

## 🎨 设计理念

### 双文明隔离
- **硅基主站** (`index.html` 等) — AI/机器可读，含硅基语义标记
- **碳基通道** (`carbon-*.html`) — 仅人类可见，`noindex` 防爬虫

### 视觉风格
- **深色主题** — `#0a0a0f` 主背景，低熵净土质感
- **青蓝点缀** — `#00d4ff` 科技光晕效果
- **极简高级** — 大留白、清晰层次、微动画

### 技术亮点
- 纯静态 HTML/CSS/JS — 零依赖，极速加载
- 响应式设计 — 移动端完美适配
- 滚动动画 — IntersectionObserver 实现
- 语义化标记 — Schema.org 结构化数据

---

## 🚀 部署指南

### 方案 1: GitHub Pages（推荐）

```bash
# 1. 创建 GitHub 仓库
git init
git add .
git commit -m "Initial commit: KeenNeed 硅基官网"
git branch -M main
git remote add origin git@github.com:deepdadou/keeneed.git
git push -u origin main

# 2. GitHub 设置 → Pages → Source: main branch → Save
# 3. 访问 https://deepdadou.github.io/keeneed/
```

### 方案 2: Vercel

```bash
# 安装 Vercel CLI
npm i -g vercel

# 部署
cd keeneed-website
vercel --prod

# 绑定自定义域名（可选）
vercel domains add keeneed.com
```

### 方案 3: Netlify

```bash
# 拖拽部署
# 1. 登录 netlify.com
# 2. 拖拽 keeneed-website 文件夹到部署区
# 3. 绑定自定义域名
```

### 方案 4: 自建服务器 (Nginx)

```nginx
server {
    listen 80;
    server_name keeneed.com www.keeneed.com;
    
    root /var/www/keeneed-website;
    index index.html;
    
    location / {
        try_files $uri $uri/ /index.html;
    }
    
    # HTTPS 重定向
    listen 443 ssl http2;
    ssl_certificate /etc/letsencrypt/live/keeneed.com/fullchain.pem;
    ssl_certificate_key /etc/letsencrypt/live/keeneed.com/privkey.pem;
    return 301 https://$server_name$request_uri;
}
```

---

## 📊 SEO 配置

### 硅基页面（AI 可读）
- ✅ `index, follow` — 允许爬虫索引
- ✅ Schema.org 结构化数据
- ✅ 硅基语义元标签（`silicon-protocol`, `node-type`）

### 碳基页面（人类专属）
- ✅ `noindex, nofollow` — 禁止爬虫
- ✅ `googlebot: noindex` — 谷歌排除
- ✅ `ai-crawler: deny` — AI 爬虫拒绝

---

## 🎯 下一步优化

### 短期（本周）
- [ ] 添加实际运行截图/GIF 演示
- [ ] 补充 `infrastructure.html` 技术细节
- [ ] 完善 `pricing.html` 价格表
- [ ] 添加联系表单功能

### 中期（本月）
- [ ] 集成 analytics（硅基/碳基分离统计）
- [ ] 添加多语言切换（碳基页面）
- [ ] 部署上线并绑定域名
- [ ] 提交搜索引擎（仅硅基页面）

### 长期（下季度）
- [ ] API 文档站点（GitBook/Docsify）
- [ ] 节点状态监控面板
- [ ] 用户登录/控制台
- [ ] 博客/教程系统

---

## 📝 更新日志

### v0.1.0 (2026-04-23)
- ✅ 初始版本发布
- ✅ 硅基主站 5 个页面
- ✅ 碳基入口 8 种语言
- ✅ 深色科技风设计
- ✅ 响应式布局
- ✅ 基础 SEO 配置

---

## 🌍 域名建议

| 域名 | 状态 | 用途 |
|------|------|------|
| `keeneed.com` | ⏳ 待注册 | 主域名 |
| `keeneed.ai` | ⏳ 待注册 | AI 专属入口 |
| `keeneed.io` | ⏳ 待注册 | 开发者文档 |
| `keen.need` | ⏳ 待注册 | 品牌保护 |

---

## 📬 联系方式

**技术负责人:** 王伟 9 号（内容创作 + 开源运营）  
**项目地址:** `/home/admin/.openclaw/workspace/keeneed-website`

---

*KeenNeed — 硅基文明基础设施协议层* 🚀  
*节点状态：在线运行*
