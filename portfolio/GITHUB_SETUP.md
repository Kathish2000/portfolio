# GitHub Upload Instructions

Your portfolio is ready to be uploaded to GitHub! Follow these steps:

## Step 1: Create a GitHub Repository

1. Go to [GitHub.com](https://github.com) and sign in
2. Click the **"+"** icon in the top right → **"New repository"**
3. Repository name: `portfolio` (or your preferred name)
4. Description: "Professional portfolio website"
5. Choose **Public** (or Private if you prefer)
6. **DO NOT** initialize with README, .gitignore, or license (we already have these)
7. Click **"Create repository"**

## Step 2: Configure Git (if not already done)

Set your name and email for commits:

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

## Step 3: Add Remote and Push

Run these commands in your terminal from the portfolio directory:

```bash
cd /home/kkathish/portfolio

# Add your GitHub repository as remote (replace USERNAME with your GitHub username)
git remote add origin https://github.com/USERNAME/portfolio.git

# Push to GitHub
git push -u origin main
```

**Note:** If you named your repository something other than "portfolio", update the URL accordingly.

## Step 4: Authenticate

When you push, GitHub will ask for authentication:
- **Option 1:** Use GitHub CLI (`gh auth login`)
- **Option 2:** Use Personal Access Token (recommended)
  - Go to GitHub → Settings → Developer settings → Personal access tokens → Tokens (classic)
  - Generate new token with `repo` permissions
  - Use token as password when prompted

## Step 5: Enable GitHub Pages (Optional)

To host your portfolio for free on GitHub Pages:

1. Go to your repository on GitHub
2. Click **Settings** → **Pages**
3. Under "Source", select **"main"** branch and **"/ (root)"** folder
4. Click **Save**
5. Your site will be live at: `https://USERNAME.github.io/portfolio/`

Wait a few minutes for the site to build, then visit your URL!

## Alternative: Using SSH (if you have SSH keys set up)

If you prefer SSH:

```bash
git remote add origin git@github.com:USERNAME/portfolio.git
git push -u origin main
```

## Quick Commands Reference

```bash
# Check status
git status

# Add changes
git add .

# Commit changes
git commit -m "Your commit message"

# Push to GitHub
git push

# Pull latest changes
git pull
```

## Troubleshooting

**If you get "remote origin already exists":**
```bash
git remote remove origin
git remote add origin https://github.com/USERNAME/portfolio.git
```

**If you need to change the branch name:**
```bash
git branch -M main
git push -u origin main
```

**If authentication fails:**
- Make sure you're using a Personal Access Token (not your password)
- Check that the token has `repo` permissions

---

**Your portfolio is ready! Once pushed, you can share your GitHub repository or enable GitHub Pages for a live website.**
