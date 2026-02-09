# Tax Title License Calculator - Vercel Deployment

A comprehensive tax title license (TTL) calculator for all 50 US states. Calculate vehicle sales tax, DMV fees, and registration costs with state-specific rules.

## 🚀 Quick Deploy to Vercel

### Option 1: Deploy via Vercel CLI

```bash
# Install Vercel CLI (if not already installed)
npm i -g vercel

# Navigate to project directory
cd vercel-ttl-calculator

# Deploy
vercel

# Follow prompts to link to your Vercel account
# Production deployment
vercel --prod
```

### Option 2: Deploy via Vercel Dashboard

1. Push this folder to GitHub
2. Go to [vercel.com](https://vercel.com)
3. Click "New Project"
4. Import your GitHub repository
5. Vercel will auto-detect the configuration
6. Click "Deploy"

### Option 3: Deploy via Git

```bash
# Initialize git repo
git init
git add .
git commit -m "Initial commit - TTL Calculator"

# Push to GitHub
git remote add origin YOUR_GITHUB_REPO_URL
git push -u origin main

# Then import to Vercel from GitHub
```

## 📁 Project Structure

```
vercel-ttl-calculator/
├── public/
│   ├── index.html           # Homepage with all states
│   ├── texas.html          # Texas TTL Calculator
│   ├── california.html     # California TTL Calculator
│   └── florida.html        # Florida TTL Calculator
├── vercel.json             # Vercel configuration
├── package.json            # Project metadata
└── README.md              # This file
```

## 🌐 URLs After Deployment

- **Homepage:** `https://your-domain.vercel.app/`
- **Texas:** `https://your-domain.vercel.app/texas-vehicle-tax-title-and-license-calculator`
- **California:** `https://your-domain.vercel.app/california-tax-title-and-license-calculator`
- **Florida:** `https://your-domain.vercel.app/florida-tax-title-and-license-calculator`

## ✨ Features

### Currently Available:
- ✅ **Texas Calculator** - SPV calculations, trade-in credit, EV fees, county-specific rates
- ✅ **California Calculator** - VLF 0.65%, NO trade-in credit, county tax rates, TIF fees
- ✅ **Florida Calculator** - Trade-in credit, surtax capping, weight-based registration

### Each Calculator Includes:
- State-specific tax rates and rules
- County/city variations
- Trade-in credit calculations (where applicable)
- DMV fee breakdowns
- Registration cost estimates
- Real-time calculations
- Mobile-responsive design
- SEO-optimized content (4,500-5,500 words per page)

## 🛠️ Technical Details

- **Framework:** Pure HTML, CSS, JavaScript (no build process needed)
- **Deployment:** Vercel static site
- **SEO:** Meta tags, structured content, state-specific keywords
- **Performance:** Lightweight, fast loading
- **Mobile:** Fully responsive design

## 📝 Custom Domain Setup (Optional)

1. Go to your Vercel project dashboard
2. Click "Settings" → "Domains"
3. Add your custom domain
4. Update DNS records as instructed
5. SSL certificate auto-configured

## 🔧 Local Development

```bash
# Serve locally (option 1 - Python)
cd public
python3 -m http.server 8000

# Serve locally (option 2 - npx)
npx serve public

# Open browser
# http://localhost:8000
```

## 📊 Analytics Setup (Optional)

Add Google Analytics or Vercel Analytics:

```html
<!-- Add to <head> of each HTML file -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

## 🎯 Next Steps

1. Deploy to Vercel
2. Test all calculator pages
3. Add remaining state calculators (47 states)
4. Set up custom domain
5. Add analytics tracking
6. Submit to search engines

## 📄 License

All rights reserved.

## 🤝 Support

For issues or questions, contact your development team.
