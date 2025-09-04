# is-a.dev 域名申请指南

## 申请 leilab-calendar.is-a.dev

### 第1步：Fork仓库
1. 访问 https://github.com/is-a-dev/register
2. 点击 **Fork** 按钮
3. 创建到你的GitHub账号下

### 第2步：创建域名文件
在你fork的仓库中，创建新文件：
- 路径：`domains/leilab-calendar.json`

文件内容：
```json
{
  "description": "Lei Lab Computer Reservation System - Tokyo Tech",
  "repo": "https://github.com/Shirakawa11111/lab-calendar",
  "owner": {
    "username": "Shirakawa11111",
    "email": "your-email@example.com"
  },
  "record": {
    "CNAME": "shirakawa11111.github.io"
  }
}
```

### 第3步：提交Pull Request
1. Commit文件（提交信息：`Add leilab-calendar domain`）
2. 创建Pull Request到原仓库
3. 标题：`Register leilab-calendar.is-a.dev`
4. 描述：
   ```
   Domain: leilab-calendar.is-a.dev
   Purpose: Lab computer reservation system for academic use
   ```

### 第4步：等待审核
- 通常24-48小时内审核
- 审核通过后会自动合并
- 域名立即生效

### 第5步：配置GitHub Pages
审核通过后，在你的仓库中：

1. 创建 `CNAME` 文件：
```bash
echo "leilab-calendar.is-a.dev" > CNAME
git add CNAME
git commit -m "Add custom domain"
git push
```

2. GitHub Settings → Pages：
   - Custom domain: `leilab-calendar.is-a.dev`
   - Save

---

## 备选域名（如果leilab-calendar被占用）

可以尝试这些：
- `leilab-booking.is-a.dev`
- `titech-leilab.is-a.dev`
- `leilab-computers.is-a.dev`
- `leilab-reserve.is-a.dev`

---

## 重要提示

### ✅ 可以做：
- 申请免费域名
- 指向GitHub Pages
- 完全免费使用

### ❌ 不能做：
- 在GitHub Custom Domain随便填写
- 必须先申请通过才能使用
- 不能使用别人已注册的域名

---

## 申请状态检查

申请后可以在这里查看状态：
https://github.com/is-a-dev/register/pulls

你的PR会显示：
- 🟡 **Open** - 等待审核
- 🟢 **Merged** - 已通过，域名可用
- 🔴 **Closed** - 被拒绝（需要修改）

---

## 最终效果

申请成功后，访问地址变为：
```
https://leilab-calendar.is-a.dev
```

比原地址简洁很多：
```
https://shirakawa11111.github.io/lab-calendar/
```

需要我帮你准备申请文件吗？