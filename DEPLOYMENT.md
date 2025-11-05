# 🚀 LayoffToLiftoff Deployment Guide

Complete instructions for deploying to GitHub Pages and setting up your custom domain with Cloudflare.

---

## 📋 Prerequisites

- [x] GitHub account (@rohimayaventures)
- [x] Repository created (financial-freedom-war)
- [ ] Domain purchased (LayoffToLiftoff.com)
- [ ] Cloudflare account

**Total Cost:** $8.03/year (domain only!)

---

## 🌐 Part 1: Deploy to GitHub Pages

### Step 1: Push Your Code
```bash
# Make sure all files are committed
git add .
git commit -m "🚀 Ready for deployment"
git push origin main
```

### Step 2: Enable GitHub Pages

1. Go to your repository on GitHub:
```
   https://github.com/rohimayaventures/financial-freedom-war
```

2. Click **Settings** (top navigation)

3. Scroll down to **Pages** (left sidebar)

4. Under **Source**:
   - Branch: `main`
   - Folder: `/ (root)`
   - Click **Save**

5. Wait 2-3 minutes for deployment

6. Your site will be live at:
```
   https://rohimayaventures.github.io/financial-freedom-war/
```

### Step 3: Test the Deployment

Visit each page to make sure everything works:
- Landing page: `/index.html`
- Pitch deck: `/pitch.html`
- Battle mode: `/battle.html`
- Demo: `/demo.html`

**✅ GitHub Pages deployment complete!**

---

## 🌍 Part 2: Buy Domain (Cloudflare)

### Step 1: Go to Cloudflare

1. Visit: https://cloudflare.com
2. Sign in or create account
3. Click **Domain Registration** (left sidebar)

### Step 2: Search for Domain

1. Search: `LayoffToLiftoff.com`
2. If available: **$8.03/year** ✅
3. Click **Purchase**
4. Complete checkout

### Step 3: Wait for Registration

- Takes 10-30 minutes
- You'll get an email confirmation
- Domain will appear in your Cloudflare dashboard

**✅ Domain purchased!**

---

## 🔗 Part 3: Connect Domain to GitHub Pages

### Step 1: Add Custom Domain in GitHub

1. Go back to GitHub repo Settings → Pages
2. Under **Custom domain**, enter:
```
   LayoffToLiftoff.com
```
3. Click **Save**
4. Check **Enforce HTTPS** (wait for it to be available)

### Step 2: Configure DNS in Cloudflare

1. Go to Cloudflare dashboard
2. Click on **LayoffToLiftoff.com**
3. Click **DNS** (left sidebar)
4. **Delete** any existing A records

5. **Add these DNS records:**

**Record 1-4: GitHub Pages A Records**
```
Type: A
Name: @
Content: 185.199.108.153
Proxy: Off (DNS only)
TTL: Auto
```

Repeat for these IPs:
- 185.199.109.153
- 185.199.110.153
- 185.199.111.153

**Record 5: CNAME for www**
```
Type: CNAME
Name: www
Content: rohimayaventures.github.io
Proxy: Off (DNS only)
TTL: Auto
```

**Record 6: CNAME for apex**
```
Type: CNAME
Name: @
Content: rohimayaventures.github.io
Proxy: Off (DNS only)
TTL: Auto
```

### Step 3: Wait for DNS Propagation

- Takes 10 minutes to 24 hours (usually ~1 hour)
- Check status: https://dnschecker.org

### Step 4: Enable Cloudflare Proxy (Optional)

Once DNS works:
1. Go back to DNS records
2. Toggle **Proxy status** to **Proxied** (orange cloud)
3. This enables Cloudflare CDN for faster loading!

**✅ Custom domain connected!**

---

## 🔒 Part 4: SSL Certificate (HTTPS)

### Automatic via GitHub Pages

1. Go to repo Settings → Pages
2. Check **Enforce HTTPS** checkbox
3. Wait 10-15 minutes for certificate

### If Issues:

1. Uncheck **Enforce HTTPS**
2. Wait 2 minutes
3. Re-check **Enforce HTTPS**
4. Wait 10 minutes

**✅ SSL enabled!**

---

## ✅ Final Checklist

- [ ] Code pushed to GitHub
- [ ] GitHub Pages enabled
- [ ] Domain purchased (LayoffToLiftoff.com)
- [ ] DNS records added in Cloudflare
- [ ] Custom domain added in GitHub
- [ ] DNS propagated (check dnschecker.org)
- [ ] HTTPS enforced
- [ ] All pages loading correctly

---

## 🎉 You're Live!

Visit your site at:
```
https://LayoffToLiftoff.com
```

**Share it with PP!** 📧

---

## 🐛 Troubleshooting

### "There isn't a GitHub Pages site here"

**Fix:** DNS hasn't propagated yet. Wait 1-24 hours.

### "Connection not secure" warning

**Fix:** HTTPS certificate still generating. Wait 10-15 minutes.

### CSS/JS not loading

**Fix:** Check file paths. Make sure they're relative:
```html
<!-- Good -->
<link rel="stylesheet" href="css/main.css">

<!-- Bad -->
<link rel="stylesheet" href="/css/main.css">
```

### Changes not showing

**Fix:** 
1. Clear browser cache (Ctrl+Shift+R)
2. Wait 2-3 minutes for GitHub Pages to rebuild
3. Check if changes were actually pushed to GitHub

---

## 💡 Pro Tips

1. **Use Cloudflare CDN** (orange cloud) for faster loading worldwide
2. **Enable Page Rules** in Cloudflare for:
   - Always Use HTTPS
   - Cache Level: Standard
3. **Set up analytics** with PostHog or Plausible
4. **Add sitemap.xml** for better SEO
5. **Submit to Google Search Console**

---

## 🚀 Next Steps

Once deployed:
1. ✅ Send link to PP
2. ✅ Post on LinkedIn
3. ✅ Share on Reddit (r/cscareerquestions, r/layoffs)
4. ✅ Launch on ProductHunt
5. ✅ Start getting users!

---

## 📧 Need Help?

- **Email:** rohimayapublishing@gmail.com
- **GitHub Issues:** Open an issue in the repo
- **Docs:** GitHub Pages docs, Cloudflare docs

---

**Built with ❤️ by Hannah + Claude**

**Total time to deploy: ~30 minutes**
**Total cost: $8.03/year**

**LET'S GOOOO!** 🚀💪🔥