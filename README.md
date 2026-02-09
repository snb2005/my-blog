# Typography Blog

A simple, static blog with no build process required.

## Structure

```
my-blog/
├── index.html          # Main blog page with all posts
├── src/                # Blog articles in markdown format
│   ├── the-unbearable-lightness-of-being.md
│   ├── tolerance-and-freedom.md
│   ├── hometown.md
│   └── rashomon.md
└── LICENSE
```

## How to Use

### Local Development
Simply open `index.html` in your browser - no build process needed!

### Hosting on GitHub Pages

1. **Push to GitHub**:
   ```bash
   git add .
   git commit -m "Simplified static blog"
   git push origin main
   ```

2. **Enable GitHub Pages**:
   - Go to your repository settings
   - Navigate to **Pages** section
   - Under **Source**, select branch: `main`
   - Select folder: `/ (root)`
   - Click **Save**

3. **Access your site**:
   - Your blog will be available at: `https://USERNAME.github.io/REPO-NAME/`

That's it! No build process, no GitHub Actions, just pure HTML.

## Features

- ✅ Single HTML file with embedded CSS
- ✅ Responsive design
- ✅ Dark mode support (automatic based on system preference)
- ✅ Clean typography
- ✅ No JavaScript required
- ✅ No build process needed
- ✅ Direct hosting from any branch

## Customization

Edit `index.html` to:
- Change colors and fonts in the `<style>` section
- Add or remove blog posts
- Update site title and links
- Customize footer information

## Adding New Posts

Simply add post content directly in the `<main>` section of `index.html` following the existing article structure, and add the full markdown file to the `src/` folder.
