# Deployment Guide - Grant Intelligence Hub

This guide provides step-by-step instructions for deploying the Grant Intelligence Hub website using various platforms, with a focus on GitHub and Vercel.

## 📋 Prerequisites

- Git installed on your computer
- GitHub account
- Basic knowledge of command line/terminal

## 🚀 Deployment Options

### Option 1: GitHub Pages (Free & Easy)

#### Step 1: Create GitHub Repository

1. **Create a new repository on GitHub:**
   - Go to [GitHub.com](https://github.com)
   - Click "New repository"
   - Name: `grant-intelligence-hub` (or your preferred name)
   - Description: "AI-powered grant management platform"
   - Make it Public
   - Initialize with README: ✅
   - Click "Create repository"

#### Step 2: Upload Your Files

**Method A: Using GitHub Web Interface**
1. Click "uploading an existing file"
2. Drag and drop all files from the `website/` folder
3. Commit changes with message: "Initial website deployment"

**Method B: Using Git Commands**
```bash
# Clone your repository
git clone https://github.com/yourusername/grant-intelligence-hub.git
cd grant-intelligence-hub

# Copy website files to repository
cp -r /path/to/website/* .

# Add, commit, and push
git add .
git commit -m "Initial website deployment"
git push origin main
```

#### Step 3: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click "Settings" tab
3. Scroll down to "Pages" section
4. Under "Source", select "Deploy from a branch"
5. Choose "main" branch and "/ (root)" folder
6. Click "Save"
7. Your site will be available at: `https://yourusername.github.io/grant-intelligence-hub`

**⏱️ Deployment Time:** 5-10 minutes

---

### Option 2: Vercel (Recommended for Production)

#### Step 1: Prepare Repository
Follow GitHub repository creation steps above.

#### Step 2: Deploy with Vercel

**Method A: Vercel Dashboard**
1. Go to [vercel.com](https://vercel.com)
2. Sign up/login with GitHub
3. Click "New Project"
4. Import your GitHub repository
5. Configure project:
   - Framework Preset: "Other"
   - Root Directory: `./` (if files are in root)
   - Build Command: (leave empty)
   - Output Directory: (leave empty)
6. Click "Deploy"

**Method B: Vercel CLI**
```bash
# Install Vercel CLI
npm i -g vercel

# Navigate to your project
cd grant-intelligence-hub

# Deploy
vercel

# Follow prompts:
# - Set up and deploy? Y
# - Which scope? (select your account)
# - Link to existing project? N
# - Project name: grant-intelligence-hub
# - In which directory is your code located? ./
```

#### Step 3: Custom Domain (Optional)
1. In Vercel dashboard, go to your project
2. Click "Settings" > "Domains"
3. Add your custom domain
4. Configure DNS records as instructed

**⏱️ Deployment Time:** 2-3 minutes
**🔄 Auto-deploy:** Yes, on every Git push

---

### Option 3: Netlify

#### Step 1: Prepare Files
Ensure all website files are in a single folder.

#### Step 2: Deploy with Netlify

**Method A: Drag & Drop**
1. Go to [netlify.com](https://netlify.com)
2. Sign up/login
3. Drag your website folder to the deploy area
4. Site will be live immediately with random URL

**Method B: Git Integration**
1. Connect GitHub repository
2. Configure build settings:
   - Build command: (leave empty)
   - Publish directory: (leave empty or `./`)
3. Deploy site

#### Step 3: Custom Domain
1. Go to Site settings > Domain management
2. Add custom domain
3. Configure DNS

**⏱️ Deployment Time:** 1-2 minutes

---

## 🔧 Advanced Configuration

### Environment Variables
If you add backend functionality later, you can set environment variables:

**Vercel:**
```bash
vercel env add VARIABLE_NAME
```

**Netlify:**
Site settings > Environment variables

### Custom Build Process
Create `package.json` for build automation:

```json
{
  "name": "grant-intelligence-hub",
  "version": "1.0.0",
  "description": "AI-powered grant management platform",
  "scripts": {
    "start": "serve .",
    "build": "echo 'No build process needed'",
    "dev": "serve . -p 3000"
  },
  "devDependencies": {
    "serve": "^14.0.0"
  }
}
```

### Performance Optimization

1. **Image Optimization:**
   ```bash
   # Install imagemin for optimization
   npm install imagemin imagemin-webp imagemin-mozjpeg imagemin-pngquant
   ```

2. **CSS Minification:**
   ```bash
   # Install cssnano
   npm install cssnano postcss-cli
   ```

3. **JavaScript Minification:**
   ```bash
   # Install terser
   npm install terser
   ```

---

## 🔍 Testing Your Deployment

### Pre-deployment Checklist
- [ ] All links work correctly
- [ ] Images load properly
- [ ] Responsive design works on mobile
- [ ] AI chat functionality works
- [ ] Forms submit correctly (if any)
- [ ] No console errors
- [ ] Fast loading times

### Testing Tools
```bash
# Local testing
python -m http.server 8000
# or
npx serve .

# Performance testing
npx lighthouse https://your-site.com

# Accessibility testing
npx pa11y https://your-site.com
```

---

## 🚨 Troubleshooting

### Common Issues

**1. GitHub Pages not updating:**
- Check Actions tab for build status
- Ensure files are in correct branch
- Clear browser cache

**2. Vercel deployment fails:**
- Check build logs in dashboard
- Verify file structure
- Ensure no syntax errors

**3. Images not loading:**
- Check file paths (case-sensitive)
- Verify image formats are supported
- Ensure images are committed to repository

**4. CSS/JS not working:**
- Check file paths in HTML
- Verify syntax in CSS/JS files
- Check browser console for errors

### Getting Help

1. **GitHub Pages Issues:**
   - [GitHub Pages Documentation](https://docs.github.com/en/pages)
   - [GitHub Community](https://github.community)

2. **Vercel Issues:**
   - [Vercel Documentation](https://vercel.com/docs)
   - [Vercel Discord](https://vercel.com/discord)

3. **Netlify Issues:**
   - [Netlify Documentation](https://docs.netlify.com)
   - [Netlify Community](https://community.netlify.com)

---

## 🔄 Continuous Deployment

### Automatic Updates
Once connected to Git, your site will automatically update when you:

1. Make changes to your code
2. Commit changes: `git commit -m "Update message"`
3. Push to GitHub: `git push origin main`
4. Platform automatically rebuilds and deploys

### Branch-based Deployments
- **Main branch:** Production site
- **Develop branch:** Staging site (Vercel/Netlify)
- **Feature branches:** Preview deployments

---

## 📊 Monitoring & Analytics

### Add Analytics
```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

### Performance Monitoring
- Use Vercel Analytics
- Set up Lighthouse CI
- Monitor Core Web Vitals

---

## 🎯 Next Steps

1. **Custom Domain:** Set up your branded domain
2. **SSL Certificate:** Ensure HTTPS (automatic on most platforms)
3. **SEO Optimization:** Add meta tags, sitemap
4. **Backend Integration:** Add contact forms, user accounts
5. **CMS Integration:** Content management system
6. **API Integration:** Connect to grant databases

---

**🎉 Congratulations!** Your Grant Intelligence Hub website is now live and ready to help organizations succeed with their grant applications.

For ongoing support and updates, bookmark this guide and check the repository for the latest improvements.