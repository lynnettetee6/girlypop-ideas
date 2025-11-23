# ✨ Cute Web App Ideas Dashboard ✨

A beautiful, interactive dashboard showcasing adorable web app ideas with a retro 90's bowtie aesthetic. Perfect for girlies who code! 💅

![Dashboard Preview](public/assets/coderpuffs_shadow.png)

## 🎀 Features

- **24 Cute Web App Ideas** across different categories
- **Interactive Filtering** by category (Productivity, Wellness, Social, Creative)
- **Retro 90's Aesthetic** with pastel colors and glassmorphism effects
- **Smooth Animations** and micro-interactions
- **Fully Responsive** design
- **Floating Decorative Elements** (stars, hearts, bows, sparkles)

## 🚀 Quick Start

### Local Development

1. Clone the repository:
```bash
git clone https://github.com/lynnettetee6/girlypop-ideas.git
cd girlypop-ideas
```

2. Open `index.html` in your browser or use a local server:
```bash
# Using Python
python3 -m http.server 8000

# Using Node.js
npx serve

# Using PHP
php -S localhost:8000
```

3. Visit `http://localhost:8000` in your browser

## 📦 Project Structure

```
girly-idea-dashboard/
├── index.html          # Main HTML file
├── style.css           # Styling with retro 90's aesthetic
├── script.js           # Interactive functionality
└── public/
    └── assets/
        └── coderpuffs_shadow.png  # Logo
```

## 🌐 Deploy to Vercel

### Option 1: Deploy via Vercel Dashboard (Recommended)

1. **Push your code to GitHub** (see instructions below)
2. **Go to [Vercel](https://vercel.com)** and sign in
3. **Click "Add New Project"**
4. **Import your GitHub repository**
5. **Click "Deploy"** - Vercel will automatically detect it's a static site
6. **Done!** Your site will be live at `https://your-project-name.vercel.app`

### Option 2: Deploy via Vercel CLI

1. **Install Vercel CLI** (if not already installed):
```bash
npm install -g vercel
```

2. **Login to Vercel**:
```bash
vercel login
```

3. **Deploy to production**:
```bash
vercel --prod
```

4. **Follow the prompts**:
   - Set up and deploy? → `Y`
   - Which scope? → Select your account
   - Link to existing project? → `N`
   - Project name? → `girly-idea-dashboard` (or your preferred name)
   - In which directory is your code located? → `./`
   - Want to modify settings? → `N`

5. **Done!** Your site will be deployed and you'll get a production URL

## 📤 Push to GitHub

If you haven't already pushed to GitHub:

1. **Create a new repository on GitHub**:
   - Go to [github.com/new](https://github.com/new)
   - Name: `girly-idea-dashboard`
   - Description: "✨ Cute Web App Ideas Dashboard - for the girlies who code 💅"
   - Make it **Public**
   - Don't initialize with README (we already have files)
   - Click "Create repository"

2. **Push your code**:
```bash
git remote add origin https://github.com/YOUR_USERNAME/girly-idea-dashboard.git
git branch -M main
git push -u origin main
```

## 🎨 Customization

### Adding New Ideas

Edit `script.js` and add new ideas to the `ideas` array:

```javascript
{
    title: "Your App Name",
    description: "Your app description",
    category: "productivity", // or wellness, social, creative
    emoji: "🎀",
    color: "var(--pink)"
}
```

### Changing Colors

Edit the CSS variables in `style.css`:

```css
:root {
    --pink: #FFB6D9;
    --purple: #D5AAFF;
    --blue: #B4E4FF;
    /* ... more colors */
}
```

## 🛠️ Technologies Used

- **HTML5** - Semantic structure
- **CSS3** - Styling with custom properties, glassmorphism, animations
- **Vanilla JavaScript** - Interactive filtering and animations
- **Google Fonts** - Fredoka & Righteous fonts

## 📝 License

Feel free to use this project for personal or commercial purposes!

## 💖 Credits

Created with love for the girlies who code! ✨

---

**Live Demo**: [https://girly-idea-dashboard.vercel.app](https://girly-idea-dashboard.vercel.app)
