# 🚀 Deployment Instructions

## Step 1: Push to GitHub

### Create a New GitHub Repository

1. Go to [github.com/new](https://github.com/new)
2. Fill in the details:
   - **Repository name**: `girly-idea-dashboard`
   - **Description**: `✨ Cute Web App Ideas Dashboard - for the girlies who code 💅`
   - **Visibility**: Public
   - **Do NOT** check "Initialize this repository with a README" (we already have files)
3. Click **"Create repository"**

### Push Your Code

After creating the repository, run these commands in your terminal:

```bash
# Navigate to your project directory
cd /Users/lynnettetee/Documents/girly-idea-dashboard

# Add the GitHub remote (replace YOUR_USERNAME with your GitHub username)
git remote add origin https://github.com/YOUR_USERNAME/girly-idea-dashboard.git

# Rename branch to main (if needed)
git branch -M main

# Push to GitHub
git push -u origin main
```

---

## Step 2: Deploy to Vercel

### Option A: Deploy via Vercel Dashboard (Easiest! ✨)

1. **Go to [vercel.com](https://vercel.com)** and sign in with your GitHub account

2. **Click "Add New Project"** (or "Import Project")

3. **Import your GitHub repository**:
   - You'll see a list of your GitHub repositories
   - Find `girly-idea-dashboard`
   - Click **"Import"**

4. **Configure your project** (usually no changes needed):
   - **Project Name**: `girly-idea-dashboard` (or customize)
   - **Framework Preset**: Vercel will auto-detect "Other" (static site)
   - **Root Directory**: `./` (leave as default)
   - **Build Command**: Leave empty (no build needed)
   - **Output Directory**: Leave empty (serves from root)

5. **Click "Deploy"**

6. **Wait for deployment** (usually takes 30-60 seconds)

7. **Done!** 🎉 Your site will be live at:
   - `https://girly-idea-dashboard.vercel.app`
   - Or a custom URL like `https://girly-idea-dashboard-xyz.vercel.app`

### Option B: Deploy via Vercel CLI

If you prefer using the command line:

```bash
# Install Vercel CLI globally (one-time setup)
npm install -g vercel

# Or use npx (no installation needed)
npx vercel --version
```

```bash
# Login to Vercel
npx vercel login
# Follow the prompts to authenticate
```

```bash
# Deploy to production
npx vercel --prod
```

**Follow the prompts**:
- `Set up and deploy?` → **Y**
- `Which scope?` → Select your account
- `Link to existing project?` → **N** (first time) or **Y** (if redeploying)
- `Project name?` → `girly-idea-dashboard`
- `In which directory is your code located?` → `./`
- `Want to modify settings?` → **N**

**Done!** You'll get a production URL like `https://girly-idea-dashboard.vercel.app`

---

## Step 3: Automatic Deployments (Optional)

Once you've connected your GitHub repository to Vercel:

- **Every push to `main` branch** will automatically deploy to production
- **Pull requests** will get preview deployments
- **No manual deployment needed!** Just `git push` and Vercel handles the rest

---

## Troubleshooting

### Issue: 404 Errors on Deployed Site

**Solution**: Make sure you don't have a `vercel.json` file. Vercel automatically serves static files correctly without any configuration.

If you have a `vercel.json`, delete it:
```bash
rm vercel.json
git add -A
git commit -m "Remove vercel.json"
git push
```

### Issue: CSS/JS Not Loading

**Solution**: Check that your file paths in `index.html` are relative:
- ✅ `<link rel="stylesheet" href="style.css">`
- ✅ `<script src="script.js"></script>`
- ✅ `<img src="public/assets/coderpuffs_shadow.png">`

### Issue: Site Requires Login

**Solution**: Make sure your Vercel project is public:
1. Go to your project settings on Vercel
2. Navigate to "General" settings
3. Ensure the project is not set to private

---

## Custom Domain (Optional)

To use a custom domain like `mycuteideas.com`:

1. Go to your Vercel project dashboard
2. Click **"Settings"** → **"Domains"**
3. Add your custom domain
4. Follow Vercel's instructions to update your DNS settings
5. Done! Your site will be available at your custom domain

---

## Quick Reference Commands

```bash
# Run locally
npm run serve
# or
python3 -m http.server 8000

# Deploy to Vercel
npm run deploy
# or
npx vercel --prod

# Push updates to GitHub
git add .
git commit -m "Your commit message"
git push
```

---

**Need help?** Check out:
- [Vercel Documentation](https://vercel.com/docs)
- [GitHub Documentation](https://docs.github.com)

✨ Happy deploying! 💅
