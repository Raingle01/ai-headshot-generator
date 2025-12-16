# KukaShot - GitHub Pages 外链页面

这是一个用于 SEO 外链建设的静态页面，托管在 GitHub Pages 上。

## 部署步骤

### 方法一：新建独立仓库（推荐）

1. **创建新的 GitHub 仓库**
   - 仓库名建议：`kukashot-ai` 或 `ai-headshot-generator`
   - 设置为 Public 仓库

2. **上传文件**
   ```bash
   # 进入 github-pages 目录
   cd github-pages
   
   # 初始化 git
   git init
   git add .
   git commit -m "Initial commit: KukaShot landing page"
   
   # 添加远程仓库并推送
   git remote add origin https://github.com/YOUR_USERNAME/kukashot-ai.git
   git branch -M main
   git push -u origin main
   ```

3. **启用 GitHub Pages**
   - 进入仓库 Settings → Pages
   - Source 选择 "Deploy from a branch"
   - Branch 选择 "main" 和 "/ (root)"
   - 点击 Save

4. **访问页面**
   - 页面将在 `https://YOUR_USERNAME.github.io/kukashot-ai/` 可访问
   - 可能需要等待几分钟才能生效

### 方法二：使用 GitHub Actions 自动部署

创建 `.github/workflows/deploy.yml`:

```yaml
name: Deploy to GitHub Pages

on:
  push:
    branches: [main]

permissions:
  contents: read
  pages: write
  id-token: write

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: actions/configure-pages@v4
      - uses: actions/upload-pages-artifact@v3
        with:
          path: '.'
      - uses: actions/deploy-pages@v4
```

## 自定义域名（可选）

1. 在 `github-pages` 目录创建 `CNAME` 文件：
   ```
   your-custom-domain.com
   ```

2. 在你的域名 DNS 设置中添加：
   - CNAME 记录指向 `YOUR_USERNAME.github.io`
   - 或 A 记录指向 GitHub Pages IP

## 页面特点

- ✅ 响应式设计，支持移动端
- ✅ 深色主题，视觉效果出众
- ✅ 包含 SEO 优化的 meta 标签
- ✅ 包含 Open Graph 社交媒体预览
- ✅ 包含 JSON-LD 结构化数据
- ✅ 所有外链指向主站 kukashot.com
- ✅ 轻量级，加载速度快

## 文件说明

- `index.html` - 主页面
- `404.html` - 404 错误页面
- `README.md` - 说明文档

## SEO 外链价值

此页面可用于：
- 社交媒体个人资料链接
- 论坛签名外链
- 目录网站提交
- 文章引用来源
- 合作伙伴外链

---

© 2024 KukaShot


