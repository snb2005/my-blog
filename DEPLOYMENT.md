# GitHub Pages Deployment Instructions

This Astro blog is now configured for automatic deployment to GitHub Pages.

## Setup Steps

### 1. Push to GitHub
First, ensure your repository is pushed to GitHub:
```bash
git add .
git commit -m "Configure for GitHub Pages deployment"
git push origin main
```

### 2. Enable GitHub Pages
1. Go to your repository on GitHub
2. Click on **Settings** > **Pages**
3. Under **Source**, select **GitHub Actions**

### 3. Configure Site URL (Important!)
Update the `site.website` value in `src/.config/user.ts` to match your GitHub Pages URL:

- For user/organization site: `https://USERNAME.github.io/`
- For project site: `https://USERNAME.github.io/REPO-NAME/`

If using a project repository (not username.github.io), also update `astro.config.ts`:
```typescript
export default defineConfig({
  site: themeConfig.site.website,
  base: '/REPO-NAME/', // Change from '/' to '/REPO-NAME/'
  // ... rest of config
})
```

### 4. Automatic Deployment
Once configured, every push to the `main` branch will automatically:
- Build your Astro site
- Deploy to GitHub Pages
- Be available at your configured URL

You can also manually trigger deployment from the **Actions** tab.

## Verification

After the first deployment:
1. Go to the **Actions** tab in your GitHub repository
2. Wait for the "Deploy to GitHub Pages" workflow to complete
3. Visit your site at the URL shown in the deployment output

## Troubleshooting

- **404 errors on pages**: Check the `base` path in `astro.config.ts`
- **Build failures**: Check the Actions log for errors
- **Site not updating**: Ensure you're pushing to the `main` branch
- **CSS/JS not loading**: Verify the `site` URL matches your actual GitHub Pages URL
