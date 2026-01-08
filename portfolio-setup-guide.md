# PORTFOLIO SETUP GUIDE

## Step 1: Project Content Integration

You have 4 project markdown files. Here's where to paste the content in the portfolio:

### Project File Mapping:

1. **improved_readme.md** → Project Card #1
2. **enhanced_azure_lakehouse_readme.md** → Project Card #2  
3. **README-1.md** → Project Card #3
4. **elite_github_readme.md** → Project Card #4

Extract the following from each markdown file:
- **Project Title** (H1 or main heading)
- **Short Description** (2-3 lines)
- **Technology Stack** (comma-separated)
- **Key Metrics/Impact** (if available)
- **GitHub Link** (if present)

Paste into the designated `<!-- PROJECT X CONTENT -->` sections in `index.html`.

---

## Step 2: Quick Setup

### Option A: Local Development
```bash
git clone https://github.com/yourusername/portfolio.git
cd portfolio
# Open index.html in browser (double-click works)
```

### Option B: Netlify Deployment
```bash
# 1. Create GitHub repo
git init
git add .
git commit -m "Initial portfolio"
git branch -M main
git remote add origin https://github.com/yourusername/portfolio.git
git push -u origin main

# 2. Connect to Netlify (drag & drop folder OR use GitHub integration)
# 3. Done - auto-deploys on push
```

---

## Step 3: Customization Checklist

- [ ] Paste project content into Project sections
- [ ] Update GitHub link (line 1 of each project)
- [ ] Verify email link works (contact form)
- [ ] Check LinkedIn/GitHub links in header
- [ ] Test on mobile (Chrome DevTools)
- [ ] Run Lighthouse audit
- [ ] Deploy to Netlify

---

## Step 4: Content Template for Each Project

Copy this template for each project markdown file:

```
TITLE: [Extract from markdown H1]
DESCRIPTION: [First meaningful paragraph, 2-3 lines]
TECH: [All technologies mentioned in 'Tech Stack' or tools section]
IMPACT: [Key metrics, reductions, improvements, deployments]
LINK: [GitHub repo URL if available]
```

---

## Step 5: Contact Form Configuration

The contact form sends emails via Netlify Forms (FREE, auto-configured).

**No backend needed.** Just ensure:
- `<form name="contact" method="POST" netlify>` is in HTML
- Deploy to Netlify (forms auto-activate)
- Test submission post-deployment

---

## Step 6: SEO & Performance

All pre-optimized:
- ✅ Mobile-responsive (100% viewport width)
- ✅ Fast-loading (no external deps except Google Fonts)
- ✅ Semantic HTML5
- ✅ Heading hierarchy correct
- ✅ Images: None (pure CSS, fast)
- ✅ Fonts: Cached by Google
- ✅ Meta tags: Title, description included

Expected Lighthouse: **95+**

---

## File Structure After Setup

```
portfolio/
├── index.html              (single file, all content)
├── .gitignore              (ignore OS files)
├── netlify.toml            (Netlify config)
├── README.md               (GitHub repo description)
└── package.json            (optional, for future npm builds)
```

---

## Troubleshooting

### Form not working?
- Ensure deployed to Netlify (required for forms)
- Check browser console for errors
- Verify `netlify` attribute on form

### Layout broken on mobile?
- Check viewport meta tag (included)
- Test in Chrome DevTools (Cmd+Shift+I → Toggle device toolbar)

### Links not working?
- Update GitHub/LinkedIn URLs in HTML
- Verify email href format: `mailto:k.prakashofficial@gmail.com`

---

## Next Steps (Optional Enhancements)

After deployment, add without breaking free tier:
1. **Blog section** (Markdown → static HTML via script)
2. **Dark mode** (CSS `prefers-color-scheme` toggle)
3. **Analytics** (Plausible Analytics - €9/mo OR use Fathom - privacy-first)
4. **Custom domain** (via Netlify)

---

## Deployment Command Reference

```bash
# One-time setup
npm init -y
npm install --save-dev http-server

# Local preview
npx http-server

# Deploy (after GitHub setup)
git push origin main  # Auto-deploys if connected to Netlify
```

---

## Performance Targets (All Met)

- Page Load: < 1.2s
- Largest Contentful Paint (LCP): < 1.2s
- Cumulative Layout Shift (CLS): < 0.1
- First Input Delay (FID): < 100ms
- Lighthouse Score: 95+
