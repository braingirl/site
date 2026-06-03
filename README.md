# The Curated Edit — Blog

A clean, minimal lifestyle blog built for GitHub Pages with affiliate links and Pinterest traffic.

---

## 🚀 Getting Started on GitHub Pages

1. Create a new GitHub repository (e.g. `my-blog` or `thecuratededit`)
2. Upload all these files to the repo
3. Go to **Settings → Pages**
4. Under "Source," select `main` branch → `/ (root)` → Save
5. Your site will be live at `https://YOURUSERNAME.github.io/YOURREPO/`

---

## ✏️ Customizing the Site

### Change the blog name
Search and replace `The Curated Edit` across all HTML files with your blog name.

### Change colors
Open `css/style.css` and edit the CSS variables at the top:
```css
:root {
  --cream: #FAF8F5;   /* page background */
  --warm: #F2EDE6;    /* card/section backgrounds */
  --text: #2A2521;    /* primary text */
  --muted: #8A847D;   /* secondary text */
  --accent: #C9A97A;  /* gold accent color */
  --rule: #E2DDD7;    /* borders */
}
```

### Add/change fonts
Fonts are loaded from Google Fonts. Change the `@import` link in `<head>` and update the CSS variables `--font-display` and `--font-body`.

---

## 📝 Adding a New Blog Post

1. Duplicate `posts/sample-post.html`
2. Rename it to a URL-friendly name: `posts/my-post-title.html`
3. Edit the `<head>` section:
   - `<title>` — your post title
   - `<meta name="description">` — 1-2 sentence description
   - `og:title`, `og:description`, `og:image` — for Pinterest previews
4. Edit the `article-header` section with your category, title, date
5. Write your content in the `article-body` div
6. Add your affiliate links using:
   ```html
   <a href="YOUR-AFFILIATE-URL" class="affiliate-link"
      rel="nofollow sponsored" target="_blank">Product Name</a>
   ```

### Add the post to the homepage
Open `index.html` and duplicate one of the `<article class="post-card">` blocks.
Update the `href`, image `src`, category, title, and excerpt.

---

## 🖼 Images

- Place images in the `/images/` folder
- **Featured post image:** `images/featured.jpg` (recommended: 800×1000px, 4:5 ratio)
- **Post hero image:** any wide image (16:9 works well)
- **Pinterest:** Use tall images (2:3 ratio, e.g. 1000×1500px) for the `og:image` tag — Pinterest favors tall pins
- **Card images:** referenced from `post-1.jpg`, `post-2.jpg` etc. in index.html

---

## 🔗 Affiliate Links

- Always add `rel="nofollow sponsored"` to affiliate links
- Always add `target="_blank"` to open in a new tab
- Use `class="affiliate-link"` for styled links
- Use the `<div class="product-callout">` block to feature a product prominently
- The affiliate disclaimer box at the top of each post is required for FTC compliance

---

## 📌 Pinterest Tips

- Set your `og:image` to a **tall 2:3 image** (e.g. 1000×1500px)
- Write a keyword-rich `og:description` — this becomes the pin description
- Add a "Save to Pinterest" button if desired (Pinterest has a free widget)
- Post titles that perform: "X Things That...", "How to...", "The Best...", "Why I Switched to..."

---

## 📁 File Structure

```
/
├── index.html          ← homepage
├── disclaimer.html     ← affiliate disclaimer (FTC required)
├── privacy.html        ← privacy policy
├── about.html          ← add this yourself
├── contact.html        ← add this yourself
├── css/
│   └── style.css       ← all styles
├── images/
│   ├── featured.jpg    ← homepage featured post image
│   ├── post-1.jpg      ← post card images
│   └── og-cover.jpg    ← homepage og:image for sharing
└── posts/
    ├── sample-post.html    ← your template, duplicate for new posts
    └── your-next-post.html
```

---

## ⚡ No Build Step Required

This is plain HTML/CSS. No Node.js, no build tools, no framework.
Just edit HTML files and push to GitHub. It works.
