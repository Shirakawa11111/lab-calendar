# Custom Domain Setup Guide | カスタムドメイン設定ガイド

## 3 Options for Custom Domain / カスタムドメインの3つの選択肢

### Option 1: Free Subdomain (Recommended) 無料サブドメイン（推奨）

#### Using **js.org** (Free for Open Source)
1. Visit https://js.org
2. Fork their GitHub repo
3. Add your subdomain request:
   ```json
   "labcalendar": "shirakawa11111.github.io/lab-calendar"
   ```
4. Create pull request
5. Get: `https://labcalendar.js.org`

#### Using **is-a.dev** (Free)
1. Visit https://is-a.dev
2. Register your subdomain
3. Point to: `shirakawa11111.github.io`
4. Get: `https://labcalendar.is-a.dev`

---

### Option 2: Custom Domain (Paid) カスタムドメイン（有料）

#### Step 1: Buy Domain / ドメイン購入
- **Namecheap**: $8-12/year
- **Google Domains**: $12/year  
- **Cloudflare**: $8-10/year
- **お名前.com** (Japan): ¥1,000-3,000/year

Example domains:
- `lab-calendar.com`
- `lab-booking.net`
- `titech-lab.com`

#### Step 2: Configure DNS / DNS設定

Add these records in your domain provider:

**A Records:**
```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

**CNAME Record:**
```
www → shirakawa11111.github.io
```

#### Step 3: GitHub Pages Setup

1. Create file in repo: `CNAME`
2. Add your domain:
   ```
   lab-calendar.com
   ```
3. Commit and push:
   ```bash
   echo "lab-calendar.com" > CNAME
   git add CNAME
   git commit -m "Add custom domain"
   git push
   ```

4. In GitHub Settings → Pages:
   - Custom domain: `lab-calendar.com`
   - Enforce HTTPS: ✅

---

### Option 3: URL Shortener (Quick Fix) 短縮URL（簡単な解決策）

#### Using **bit.ly** (Free)
1. Visit https://bit.ly
2. Paste: `https://shirakawa11111.github.io/lab-calendar/`
3. Get short URL like: `bit.ly/lab-cal`

#### Using **TinyURL** (Free)
1. Visit https://tinyurl.com
2. Custom alias: `tinyurl.com/titech-lab`

#### Using **Rebrandly** (Free tier)
1. Visit https://rebrandly.com
2. Create branded link
3. Get: `lab.link/calendar`

---

## Recommended Solution / 推奨ソリューション

### For Professional Look:
**Buy a domain** from Namecheap (~$10/year)
- `labcomputers.net`
- `lab-reserve.com`

### For Free Solution:
**Use is-a.dev**
- Apply at: https://is-a.dev
- Get: `labcalendar.is-a.dev`
- Professional looking & free

### For Quick Sharing:
**Use bit.ly**
- Create: `bit.ly/lab-computers`
- Easy to share & remember

---

## Implementation Steps / 実装手順

### If you choose custom domain:

1. **Buy domain** (10 minutes)
2. **Add DNS records** (5 minutes)  
3. **Add CNAME file to repo** (2 minutes)
4. **Wait for propagation** (10-60 minutes)
5. **Done!** Access via `yourlab.com`

### Current URL:
```
https://shirakawa11111.github.io/lab-calendar/
```

### After custom domain:
```
https://lab-calendar.com
```

---

## Need Help? / ヘルプが必要？

Let me know which option you prefer:
1. Free subdomain (js.org / is-a.dev)
2. Buy custom domain
3. URL shortener

I can help you set it up!

どのオプションがお好みか教えてください。設定をお手伝いします！