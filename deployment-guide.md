# 部署指南 - 让大家都能访问

## 方法1: GitHub Pages（推荐）✅

### 步骤：
1. **创建GitHub账号**（如果没有）
   - 访问 https://github.com
   - 注册账号

2. **创建新仓库**
   - 点击右上角 "+" → "New repository"
   - 仓库名称：`lab-calendar`
   - 设置为Public（公开）
   - 创建仓库

3. **上传文件**
   ```bash
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/lab-calendar.git
   git push -u origin main
   ```

4. **启用GitHub Pages**
   - 进入仓库设置 Settings
   - 左侧找到 Pages
   - Source 选择 "Deploy from a branch"
   - Branch 选择 "main" → "/ (root)"
   - 点击 Save

5. **访问地址**
   - 等待几分钟
   - 访问：`https://YOUR_USERNAME.github.io/lab-calendar/`

## 方法2: Vercel（免费，自动部署）

1. 访问 https://vercel.com
2. 用GitHub账号登录
3. Import Git Repository
4. 选择你的仓库
5. 自动部署，获得网址

## 方法3: 实验室服务器

### 使用Python简单服务器：
```bash
# 在calendar文件夹中运行
python3 -m http.server 8000
```
访问：`http://服务器IP:8000`

### 使用Node.js：
```bash
# 安装http-server
npm install -g http-server

# 运行
http-server -p 8080
```
访问：`http://服务器IP:8080`

### 使用Nginx：
```nginx
server {
    listen 80;
    server_name lab.example.com;
    root /var/www/lab-calendar;
    index index.html;
}
```

## 方法4: 云存储共享

### 腾讯微云/百度网盘
1. 上传HTML文件
2. 生成共享链接
3. 设置永久有效
4. 分享给实验室成员

### OneDrive
1. 上传到OneDrive
2. 右键 → 共享
3. 获取链接
4. 任何人都可以查看

## 方法5: 内网NAS

如果实验室有NAS：
1. 创建共享文件夹
2. 上传HTML文件
3. 开启Web服务
4. 内网访问：`http://NAS_IP/lab-calendar/`

## 最简单方案总结

### 立即使用（5分钟）：
1. **GitHub Pages**
   - 创建GitHub账号
   - 拖拽上传文件
   - 开启Pages
   - 完成！

### 访问地址示例：
```
https://labname.github.io/calendar/
```

## 注意事项

1. **替换日历ID**
   - 必须先替换`YOUR_CALENDAR_ID_1`等
   - 否则日历不会显示

2. **权限设置**
   - Google Calendar必须设置为"公开"或正确共享
   - 否则其他人看不到内容

3. **HTTPS要求**
   - GitHub Pages自带HTTPS
   - 自建服务器建议配置SSL证书

需要我帮你执行哪种部署方式？