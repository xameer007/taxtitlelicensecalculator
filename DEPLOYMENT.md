# Step-by-Step Vercel Deployment Guide

## 🎯 Complete Deployment Instructions

### Prerequisites
- Vercel account (free): https://vercel.com/signup
- Git installed (optional but recommended)

---

## Method 1: Quick Deploy (Drag & Drop) - EASIEST

### Step 1: Download Project
1. Download the entire `vercel-ttl-calculator` folder
2. Create a ZIP file of the folder (if needed)

### Step 2: Deploy to Vercel
1. Go to https://vercel.com
2. Click "Add New..." → "Project"
3. Click "Deploy from ZIP"
4. Drag and drop your folder or select the ZIP file
5. Click "Deploy"
6. Wait 30-60 seconds
7. ✅ Done! Your site is live

**Your URLs will be:**
- Homepage: `https://your-project-name.vercel.app`
- Texas: `https://your-project-name.vercel.app/texas-vehicle-tax-title-and-license-calculator`
- California: `https://your-project-name.vercel.app/california-tax-title-and-license-calculator`
- Florida: `https://your-project-name.vercel.app/florida-tax-title-and-license-calculator`

---

## Method 2: Deploy via GitHub (Recommended for Updates)

### Step 1: Create GitHub Repository
1. Go to https://github.com/new
2. Repository name: `ttl-calculator`
3. Set to Public or Private
4. Click "Create repository"

### Step 2: Upload Code to GitHub
```bash
# Navigate to project folder
cd vercel-ttl-calculator

# Initialize git
git init

# Add all files
git add .

# Commit
git commit -m "Initial commit - TTL Calculator"

# Add remote (replace with your repo URL)
git remote add origin https://github.com/YOUR_USERNAME/ttl-calculator.git

# Push to GitHub
git branch -M main
git push -u origin main
```

### Step 3: Deploy from GitHub to Vercel
1. Go to https://vercel.com/new
2. Click "Import Git Repository"
3. Select your `ttl-calculator` repo
4. Vercel auto-detects configuration
5. Click "Deploy"
6. ✅ Done! Auto-deploys on every git push

---

## Method 3: Deploy via Vercel CLI

### Step 1: Install Vercel CLI
```bash
npm install -g vercel
```

### Step 2: Login to Vercel
```bash
vercel login
```

### Step 3: Deploy
```bash
# Navigate to project
cd vercel-ttl-calculator

# Deploy to preview
vercel

# Deploy to production
vercel --prod
```

---

## 🌐 Custom Domain Setup (Optional)

### After Deployment:
1. Go to your Vercel project dashboard
2. Click "Settings" → "Domains"
3. Click "Add Domain"
4. Enter your domain: `ttlcalculator.com`
5. Vercel provides DNS instructions
6. Update your domain registrar DNS:
   - Add A record: `76.76.21.21`
   - Or CNAME: `cname.vercel-dns.com`
7. Wait 24-48 hours for DNS propagation
8. SSL certificate auto-issued

---

## 📱 Testing Your Deployment

### Test These URLs:
```
✅ Homepage
https://your-domain.vercel.app/

✅ Texas Calculator
https://your-domain.vercel.app/texas-vehicle-tax-title-and-license-calculator

✅ California Calculator  
https://your-domain.vercel.app/california-tax-title-and-license-calculator

✅ Florida Calculator
https://your-domain.vercel.app/florida-tax-title-and-license-calculator
```

### Verify:
- [ ] All pages load correctly
- [ ] Calculators work on desktop
- [ ] Calculators work on mobile
- [ ] Internal navigation works
- [ ] All links function properly

---

## 🔄 Making Updates After Deployment

### If deployed via GitHub:
```bash
# Make changes to files
# Then:
git add .
git commit -m "Update calculator"
git push

# Vercel auto-deploys in 30-60 seconds
```

### If deployed via drag & drop:
1. Make changes locally
2. Go to Vercel dashboard
3. Click your project
4. Click "Deployments" tab
5. Drag new folder or use Vercel CLI to update

---

## 🎨 Customization Options

### Change Site Name:
1. Go to Vercel dashboard
2. Project Settings → General
3. Change "Project Name"
4. URLs update automatically

### Add More States:
1. Create new HTML file: `public/state-name.html`
2. Add route in `vercel.json`:
```json
{
  "src": "/state-name-ttl-calculator",
  "dest": "/public/state-name.html"
}
```
3. Update homepage links
4. Deploy

---

## 📊 Analytics Setup (Optional)

### Google Analytics:
1. Get GA4 Measurement ID
2. Add to each HTML file in `<head>`:
```html
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

### Vercel Analytics (Built-in):
1. Go to project dashboard
2. Click "Analytics" tab
3. Enable analytics
4. Free tier: 100k events/month

---

## 🚨 Troubleshooting

### Pages showing 404:
- Check `vercel.json` routes
- Ensure file exists in `public/` folder
- Redeploy

### Calculator not working:
- Check browser console for JavaScript errors
- Verify all form IDs match JavaScript selectors
- Test on different browsers

### Slow loading:
- Enable Vercel Edge Network (automatic)
- Compress images if added later
- Minify CSS/JS (optional)

---

## ✅ Deployment Checklist

- [ ] All files in `vercel-ttl-calculator/` folder
- [ ] `public/` folder contains all HTML files
- [ ] `vercel.json` configured correctly
- [ ] Deployed to Vercel
- [ ] All 4 pages tested (home + 3 calculators)
- [ ] Mobile responsive verified
- [ ] Custom domain added (optional)
- [ ] Analytics configured (optional)
- [ ] SSL certificate active (automatic)

---

## 🎉 You're Done!

Your Tax Title License Calculator is now live and accessible worldwide!

**Share your calculators:**
- Social media
- Car forums
- Auto dealership partnerships
- SEO/Google indexing

**Next steps:**
1. Add remaining 47 state calculators
2. Build backlinks for SEO
3. Submit sitemap to Google Search Console
4. Monitor analytics
