# 客户管理系统

## 项目介绍

这是一个专为美国中餐馆和实体企业设计的客户管理系统，具有以下功能：
- 客户信息管理
- 销售跟进管理
- 交付管理
- 续费管理
- 财务管理
- 任务协作
- 数据统计和报表

## 技术栈

- 前端：HTML5, Tailwind CSS, JavaScript, Chart.js
- 后端：Supabase (PostgreSQL数据库)

## 系统设置

### 1. Supabase 配置

1. 访问 [Supabase](https://supabase.com) 并创建一个新项目
2. 在项目设置中获取以下信息：
   - Project URL
   - Anon Key
3. 编辑以下文件，将占位符替换为实际的Supabase配置：
   - `customers.html` (第606-607行)
   - `dashboard.html` (第394-395行)

### 2. 数据库表结构

在Supabase中创建以下表：

#### customers 表

| 字段名 | 数据类型 | 约束 | 描述 |
|--------|---------|------|------|
| id | int8 | primary key | 客户ID |
| customer_number | text | unique | 客户编号 |
| business_name | text | not null | 商家名称 |
| contact_person | text | not null | 联系人 |
| phone | text | not null | 联系电话 |
| wechat_whatsapp | text | | 微信/WhatsApp |
| email | text | | 邮箱 |
| industry | text | not null | 行业类型 |
| business_address | text | | 商家地址 |
| city | text | | 城市 |
| state | text | | 州 |
| customer_source | text | | 客户来源 |
| sales_person | text | | 负责人 |
| level | text | | 客户等级 |
| status | text | default 'unclosed' | 客户状态 |
| has_ordering_system | boolean | | 是否已有线上点餐系统 |
| current_platform | text | | 当前使用的平台 |
| monthly_orders | int4 | | 月订单量 |
| website | text | | 商家官网 |
| google_business | text | | Google Business 链接 |
| facebook | text | | Facebook 链接 |
| instagram | text | | Instagram 链接 |
| yelp | text | | Yelp 链接 |
| notes | text | | 备注 |
| created_at | timestamptz | default now() | 创建时间 |

### 3. 本地开发

1. 克隆项目到本地
2. 在项目根目录启动本地服务器：
   ```bash
   python3 -m http.server 8000
   ```
3. 访问 http://localhost:8000 查看系统

### 4. 部署

可以将项目部署到任何静态网站托管服务，如：
- GitHub Pages
- Vercel
- Netlify
- AWS S3

## 系统使用

### 登录

使用以下演示账号登录：
- 管理员: admin / password
- 销售: sales / password
- 运营: operation / password
- 设计: design / password
- 财务: finance / password

### 功能说明

1. **客户管理**：添加、查看、编辑和删除客户信息
2. **销售管理**：管理销售线索和跟进记录
3. **交付管理**：跟踪项目交付进度
4. **续费管理**：管理客户续费事宜
5. **财务管理**：记录收支情况
6. **任务协作**：分配和跟踪任务
7. **报表中心**：查看系统数据统计和分析

## 常见问题

### 无法添加客户
- 检查Supabase配置是否正确
- 确保customers表已创建且结构正确
- 检查浏览器控制台是否有错误信息

### 无法删除客户
- 检查Supabase配置是否正确
- 确保用户有删除权限
- 检查浏览器控制台是否有错误信息

### 数据不显示
- 检查Supabase配置是否正确
- 确保数据库中有数据
- 检查浏览器控制台是否有错误信息

## 技术支持

如有任何问题，请联系技术支持团队。