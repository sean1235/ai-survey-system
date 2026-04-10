# 🚀 立即部署 - 3分钟上线

## 方法1：一键部署到Vercel（最简单）

### 步骤1：准备MongoDB连接字符串

1. 访问：https://www.mongodb.com/cloud/atlas/register
2. 注册并创建免费集群（选择新加坡区域）
3. 创建数据库用户，获取连接字符串：
   ```
   mongodb+srv://用户名:密码@cluster.xxxxx.mongodb.net/?retryWrites=true&w=majority
   ```

### 步骤2：点击下面的按钮部署

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/你的用户名/survey-system&env=MONGODB_URI&envDescription=MongoDB%20Atlas%20connection%20string)

**或者手动部署：**

1. 访问：https://vercel.com
2. 用GitHub登录
3. 点击"Add New" → "Project"
4. 选择"Import Git Repository"
5. 粘贴这个文件夹的路径或上传到GitHub
6. 添加环境变量：
   - Name: `MONGODB_URI`
   - Value: 你的MongoDB连接字符串
7. 点击"Deploy"

---

## 方法2：使用Vercel CLI（推荐给技术用户）

### 安装Vercel CLI

```bash
npm install -g vercel
```

### 登录Vercel

```bash
vercel login
```

### 部署项目

```bash
# 在项目文件夹执行
vercel

# 按提示操作，然后添加环境变量
vercel env add MONGODB_URI production

# 输入你的MongoDB连接字符串

# 生产环境部署
vercel --prod
```

---

## 方法3：通过GitHub自动部署

### 1. 创建GitHub仓库

访问：https://github.com/new

- 仓库名：survey-system
- 类型：Public
- 点击"Create repository"

### 2. 推送代码

在项目文件夹执行：

```bash
git remote add origin https://github.com/你的用户名/survey-system.git
git branch -M main
git push -u origin main
```

### 3. 连接Vercel

1. 访问 https://vercel.com
2. 点击"Import Project"
3. 选择你的GitHub仓库
4. 添加环境变量 `MONGODB_URI`
5. 点击"Deploy"

---

## 🎯 部署后的访问地址

部署成功后，你会得到：

```
https://survey-system-xxxx.vercel.app
```

### 四个页面：

1. **首页**：https://你的域名.vercel.app/
2. **学生问卷**：https://你的域名.vercel.app/student-survey.html
3. **教师问卷**：https://你的域名.vercel.app/teacher-survey.html
4. **数据管理**：https://你的域名.vercel.app/admin.html

---

## ✅ 验收测试

部署完成后，请测试：

1. ✅ 访问首页，两个卡片可以点击
2. ✅ 填写并提交学生问卷
3. ✅ 填写并提交教师问卷
4. ✅ 访问管理后台，看到提交的数据
5. ✅ 查看图表是否正常显示
6. ✅ 导出Excel测试

---

## 🆘 遇到问题？

### 问题1：部署失败

- 检查MongoDB连接字符串是否正确
- 确保密码中的特殊字符已URL编码

### 问题2：数据不显示

- 打开浏览器F12开发者工具
- 查看Console是否有错误
- 检查Network标签，API请求是否成功

### 问题3：国内访问慢

- MongoDB选择新加坡区域
- Vercel自动使用CDN，已经很快

---

## 📞 需要帮助？

查看详细文档：
- QUICK_START.md - 快速启动
- DEPLOYMENT_GUIDE.md - 完整指南
- CHECKLIST.md - 检查清单

---

**准备好了吗？开始部署吧！** 🚀
