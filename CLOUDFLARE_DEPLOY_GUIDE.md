# Cloudflare Pages 部署指南

## 📋 部署前准备

### 1. 准备工作
- ✅ GitHub 仓库已创建：`xianjian1211/jiankang`
- ✅ 项目文件已上传（index.html 等文件）
- ✅ 注册 Cloudflare 账号（免费）

---

## 🚀 部署步骤

### 步骤 1：注册 Cloudflare 账号（如果还没有）

1. 访问 Cloudflare 官网：https://dash.cloudflare.com/sign-up
2. 使用邮箱注册（免费）
3. 完成邮箱验证

---

### 步骤 2：创建 Pages 项目

1. 登录 Cloudflare Dashboard
2. 在左侧菜单找到 **Workers & Pages**
3. 点击 **Create application**
4. 点击 **Pages** 标签
5. 点击 **Create application** 按钮
6. 选择 **Connect to Git**

---

### 步骤 3：连接 GitHub 仓库

1. 点击 **Connect to GitHub** 按钮
2. 系统会跳转到 GitHub 授权页面
3. 点击 **Authorize Cloudflare** 授权 Cloudflare 访问您的 GitHub
4. 授权成功后，会显示您的 GitHub 仓库列表
5. 找到并选择 **jiankang** 仓库

---

### 步骤 4：配置构建设置

由于本项目是纯静态 HTML 项目，不需要构建过程，配置如下：

#### Project Settings（项目设置）

| 配置项 | 值 | 说明 |
|--------|-----|------|
| **Project name** | `dialysis-health-system` | 项目名称（可自定义） |
| **Production branch** | `main` | 生产分支 |
| **Framework preset** | `None` | 无需框架（纯静态） |
| **Build command** | （留空） | 无需构建 |
| **Build output directory** | `/` | 根目录 |
| **Root directory** | `/` | 根目录 |

#### Environment variables（环境变量）
- 无需配置

---

### 步骤 5：开始部署

1. 点击 **Save and Deploy** 按钮
2. 等待部署完成（通常需要 1-2 分钟）
3. 部署成功后会显示访问地址

---

## ✅ 部署成功

### 访问您的网站

部署成功后，您会得到以下访问地址：

```
https://dialysis-health-system.pages.dev
```

或者根据您的项目名称：
```
https://您的项目名.pages.dev
```

---

## 🔧 自定义域名（可选）

如果需要使用自定义域名（如 `health.yourdomain.com`）：

1. 在 Cloudflare Pages 项目中点击 **Custom domains**
2. 点击 **Set up a custom domain**
3. 输入您的域名
4. 按照提示完成 DNS 配置

---

## 📊 常用管理操作

### 查看部署历史
- 进入项目详情
- 点击 **Deployments** 标签
- 查看所有部署记录

### 重新部署
- 方法1：推送代码到 GitHub 会自动触发部署
- 方法2：在 Cloudflare Pages 点击 **Retry deployment**

### 回滚到之前版本
- 在 Deployments 列表中找到之前的版本
- 点击 **Rollback**

---

## 🌐 部署后的优势

### Cloudflare Pages 免费版特性

- ✅ **无限带宽**：无流量限制
- ✅ **无限请求**：无访问次数限制
- ✅ **全球 CDN**：200+ 节点，全球加速
- ✅ **自动 HTTPS**：免费 SSL 证书
- ✅ **自动部署**：代码推送自动构建
- ✅ **预览环境**：每个 Pull Request 自动生成预览
- ✅ **函数支持**：支持 Cloudflare Workers
- ✅ **自定义域名**：支持绑定自有域名

---

## ⚠️ 注意事项

1. **GitHub 仓库必须是公开的**
   - 如果是私有仓库，需要配置访问权限

2. **index.html 必须在根目录**
   - Cloudflare Pages 默认会查找根目录的 index.html

3. **文件大小限制**
   - 单个文件最大 25MB
   - 总文件数量最大 20,000 个

4. **访问速度**
   - 国内访问速度：⭐⭐⭐⭐（良好）
   - 海外访问速度：⭐⭐⭐⭐⭐（极佳）

---

## 🆘 常见问题

### Q1: 部署失败怎么办？
**A:**
1. 检查 GitHub 仓库是否公开
2. 检查 index.html 是否在根目录
3. 查看 Deployment 日志了解具体错误

### Q2: 如何更新网站？
**A:** 只需推送代码到 GitHub，Cloudflare Pages 会自动重新部署：
```bash
git add .
git commit -m "更新内容"
git push origin main
```

### Q3: 可以同时部署到多个平台吗？
**A:** 可以！您可以同时部署到：
- Cloudflare Pages（全球访问）
- Gitee Pages（国内加速）
- GitHub Pages（备用）

### Q4: 如何删除项目？
**A:**
1. 进入 Cloudflare Pages
2. 选择项目
3. 点击 Settings
4. 滚动到底部点击 **Delete project**

---

## 📞 技术支持

- Cloudflare Pages 文档：https://developers.cloudflare.com/pages/
- Cloudflare 社区：https://community.cloudflare.com/

---

**祝您部署顺利！🎉**
