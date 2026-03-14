# 客户管理系统部署指南

## 部署选项

### 1. GitHub Pages 部署（推荐）

GitHub Pages 是一个免费的静态网站托管服务，适合部署我们的客户管理系统。

**部署步骤：**

1. **创建 GitHub 仓库**
   - 登录 GitHub 账号
   - 点击 "New repository"
   - 输入仓库名称（例如：customer-management-system）
   - 选择 "Public" 或 "Private"
   - 点击 "Create repository"

2. **推送代码到 GitHub**
   - 在本地终端中执行以下命令：
     ```bash
     # 添加远程仓库
     git remote add origin https://github.com/your-username/customer-management-system.git
     
     # 推送代码
     git push -u origin main
     ```

3. **启用 GitHub Pages**
   - 进入 GitHub 仓库页面
   - 点击 "Settings" 标签
   - 滚动到 "Pages" 部分
   - 在 "Source" 下拉菜单中选择 "main" 分支
   - 点击 "Save"
   - 等待几分钟，GitHub 会生成部署 URL

4. **访问系统**
   - 部署完成后，您可以通过生成的 URL 访问系统（例如：https://your-username.github.io/customer-management-system）

### 2. Vercel 部署

Vercel 是一个现代化的静态网站托管平台，提供免费的部署服务。

**部署步骤：**

1. **创建 Vercel 账号**
   - 访问 https://vercel.com/ 并注册账号

2. **导入项目**
   - 登录 Vercel 控制台
   - 点击 "Import Project"
   - 选择 "Import Git Repository"
   - 粘贴 GitHub 仓库 URL
   - 点击 "Import"

3. **配置部署**
   - 保持默认配置
   - 点击 "Deploy"

4. **访问系统**
   - 部署完成后，Vercel 会生成一个 URL，您可以通过该 URL 访问系统

### 3. 传统服务器部署

如果您有自己的服务器，可以通过以下步骤部署：

1. **准备服务器**
   - 确保服务器安装了 Web 服务器软件（如 Nginx、Apache）
   - 确保服务器可以访问互联网

2. **上传代码**
   - 使用 FTP、SFTP 或 Git 等方式将代码上传到服务器
   - 例如，使用 Git 克隆：
     ```bash
     git clone https://github.com/your-username/customer-management-system.git /var/www/html/
     ```

3. **配置 Web 服务器**
   - 配置 Nginx 或 Apache 指向您的代码目录
   - 例如，Nginx 配置：
     ```nginx
     server {
         listen 80;
         server_name your-domain.com;
         root /var/www/html/customer-management-system;
         index index.html;
         
         location / {
             try_files $uri $uri/ /index.html;
         }
     }
     ```

4. **访问系统**
   - 通过服务器的 IP 地址或域名访问系统

## 系统访问

部署完成后，您可以通过以下方式访问系统：

1. **登录页面**：访问部署 URL（例如：https://your-username.github.io/customer-management-system）
2. **登录账号**：
   - 超级管理员：super_admin / password
   - 管理员：admin / password
   - 销售：sales / password
   - 运营：operations / password
   - 设计：designer / password
   - 财务：finance / password
   - 人事：hr / password

## 注意事项

1. **数据存储**：当前系统使用本地存储（localStorage）存储数据，数据仅存储在用户浏览器中，不会同步到服务器。如果需要服务器端存储，建议后续集成后端数据库。

2. **安全性**：
   - 登录密码仅做简单验证，建议在生产环境中使用更安全的认证方式
   - 敏感数据未加密存储，建议在生产环境中添加加密措施

3. **性能优化**：
   - 对于大型客户数据，可能需要优化本地存储的使用
   - 考虑使用索引数据库（IndexedDB）存储大量数据

4. **浏览器兼容性**：
   - 系统支持现代浏览器（Chrome、Firefox、Safari、Edge）
   - 不支持 IE 浏览器

## 后续维护

1. **代码更新**：
   - 本地修改代码后，提交并推送到 GitHub
   - GitHub Pages 和 Vercel 会自动重新部署

2. **功能扩展**：
   - 可以根据需要添加新功能
   - 建议遵循现有的代码结构和命名规范

3. **问题排查**：
   - 如遇问题，检查浏览器控制台的错误信息
   - 确保本地存储有足够的空间
   - 检查网络连接是否正常

## 联系支持

如果在部署过程中遇到问题，可以参考以下资源：

- GitHub Pages 文档：https://docs.github.com/en/pages
- Vercel 文档：https://vercel.com/docs
- 系统设计文档：system-design.md

祝您使用愉快！