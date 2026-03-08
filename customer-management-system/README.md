# 客户管理系统 (Customer Management System)

专为美国中餐馆和实体企业设计的客户管理系统，提供客户信息管理、销售跟进、交付管理、续费管理、财务收款和员工协作等功能。

## 系统功能

### 核心模块
- **客户管理**：客户信息管理、客户分类、客户搜索和筛选
- **销售管理**：销售线索管理、跟进记录、成交管理、销售漏斗分析
- **交付管理**：交付项目管理、任务分配、进度跟踪、交付统计
- **续费管理**：续费提醒、续费记录、套餐管理、续费统计
- **财务管理**：收款记录、财务统计、收支分析
- **系统设置**：用户管理、角色权限设置、系统配置

### 技术特点
- 响应式设计，支持PC端和移动端
- 基于HTML5和Tailwind CSS构建，界面美观现代
- 内置图表和数据可视化
- 本地存储会话管理
- 角色-based权限控制
- 模块化设计，易于扩展

## 快速开始

### 本地运行
1. 克隆项目到本地
2. 直接打开 `index.html` 文件即可运行
3. 使用以下测试账号登录：
   - 管理员：admin / password (所有权限)
   - 销售：sales / password (销售相关权限)
   - 运营：operation / password (运营相关权限)
   - 设计：design / password (设计相关权限)
   - 财务：finance / password (财务相关权限)

### 部署上线

#### 方法1：GitHub Pages
1. 在GitHub上创建一个新仓库
2. 将项目推送到GitHub仓库
3. 在仓库设置中开启GitHub Pages功能
4. 选择 `main` 分支作为源
5. 访问生成的GitHub Pages URL

#### 方法2：Vercel
1. 访问 [Vercel](https://vercel.com/)
2. 登录或注册账号
3. 点击 "New Project"
4. 导入GitHub仓库
5. 点击 "Deploy" 按钮
6. 访问生成的Vercel URL

#### 方法3：Netlify
1. 访问 [Netlify](https://www.netlify.com/)
2. 登录或注册账号
3. 点击 "Add new site"
4. 选择 "Import an existing project"
5. 连接GitHub仓库
6. 点击 "Deploy site"
7. 访问生成的Netlify URL

## 项目结构

```
├── index.html          # 登录页面
├── dashboard.html      # 仪表盘页面
├── customers.html      # 客户管理页面
├── sales.html          # 销售管理页面
├── delivery.html       # 交付管理页面
├── renewal.html        # 续费管理页面
├── finance.html        # 财务管理页面
├── settings.html       # 系统设置页面
├── system-design.md    # 系统设计文档
└── README.md           # 项目说明文档
```

## 技术栈

- **前端框架**：HTML5, Tailwind CSS v3
- **JavaScript**：原生JavaScript
- **图表库**：Chart.js
- **图标库**：Font Awesome
- **存储**：LocalStorage (本地存储)
- **响应式设计**：Tailwind CSS 响应式类

## 系统设计

详细的系统设计文档请参考 `system-design.md` 文件。

## 注意事项

1. 本系统使用LocalStorage进行数据存储，仅适用于演示和测试环境
2. 生产环境建议使用后端数据库存储数据
3. 系统已内置模拟数据，方便直接查看功能
4. 可根据实际业务需求修改和扩展功能

## 许可证

MIT License
