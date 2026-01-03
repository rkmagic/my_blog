# SEO Guide for Your Jekyll Blog

This document outlines the SEO optimizations implemented and best practices for maintaining good SEO on your blog.

## ✅ What's Already Implemented

### 1. **Automatic SEO Meta Tags** (via jekyll-seo-tag plugin)
- The `jekyll-theme-yat` theme includes `jekyll-seo-tag` plugin
- Automatically generates:
  - Title tags
  - Meta descriptions
  - Open Graph tags (for Facebook, LinkedIn)
  - Twitter Card tags
  - Canonical URLs
  - Structured data (JSON-LD schema)

### 2. **Sitemap Generation**
- `jekyll-sitemap` plugin automatically generates `sitemap.xml`
- Helps search engines discover all your pages

### 3. **RSS Feed**
- `jekyll-feed` plugin generates `feed.xml`
- Helps with content discovery and syndication

### 4. **robots.txt**
- Created to guide search engine crawlers
- Points to your sitemap location

## 📋 Required Actions

### 1. **Set Your Site URL** (CRITICAL)
In `_config.yml`, update the `url` field with your actual domain:

```yaml
url: "https://yourdomain.com"  # Replace with your actual domain
```

**Why this matters:** Without the correct URL, canonical links won't work properly, which can hurt SEO.

### 2. **Optional: Add Twitter Username**
If you have a Twitter account, add it to `_config.yml`:

```yaml
twitter:
  username: yourusername  # Without the @ symbol
```

### 3. **Optional: Add Default Images**
For better social media sharing, add default images to `_config.yml`:

```yaml
logo: "/assets/images/logo.png"  # Your site logo
image: "/assets/images/banner.webp"  # Default Open Graph image
```

## 📝 Best Practices for Blog Posts

### 1. **Add Excerpts/Descriptions**
Add an `excerpt` or `description` field to your post front matter for better meta descriptions:

```yaml
---
layout: post
title: "Your Post Title"
date: 2024-01-01 12:00:00 +0530
categories: category
excerpt: "A compelling 150-160 character description of your post that will appear in search results and social media previews."
---
```

**Tip:** If you don't add an excerpt, Jekyll will use the first paragraph, which may not be optimized.

### 2. **Use Descriptive Titles**
- Keep titles between 50-60 characters
- Include relevant keywords naturally
- Make them compelling and clickable

### 3. **Optimize Images**
Add descriptive `alt` text to all images:

```markdown
![Description of what the image shows](/path/to/image.jpg)
```

**Why:** Alt text helps with:
- Accessibility (screen readers)
- SEO (search engines understand image content)
- Image search rankings

### 4. **Use Proper Heading Structure**
- One `<h1>` per page (usually the title)
- Use `<h2>`, `<h3>`, etc. in hierarchical order
- Include keywords in headings naturally

### 5. **Add Keywords (Optional)**
You can add keywords to post front matter (though less important than before):

```yaml
---
keywords: ["keyword1", "keyword2", "keyword3"]
---
```

## 🔍 Additional SEO Enhancements

### Internal Linking
- Link to other relevant posts on your blog
- Use descriptive anchor text (not "click here")
- Helps with both SEO and user engagement

### External Linking
- Link to authoritative sources
- Shows you've done research
- Can improve credibility

### Content Quality
- Write comprehensive, valuable content
- Answer user questions thoroughly
- Update old posts with new information

### Mobile Optimization
- Your theme should be responsive (jekyll-theme-yat is)
- Test your site on mobile devices
- Ensure fast load times

## 🛠️ Tools to Monitor SEO

1. **Google Search Console**
   - Submit your sitemap
   - Monitor search performance
   - Find and fix issues

2. **Google Analytics** (or Vercel Analytics - already integrated)
   - Track visitor behavior
   - Understand what content performs well

3. **PageSpeed Insights**
   - Check site speed
   - Get optimization suggestions

4. **Schema Markup Validator**
   - Validate structured data: https://validator.schema.org/

## 📊 Checking Your SEO

After deployment, verify:

1. **Meta Tags**: View page source and check for:
   - `<title>` tag
   - `<meta name="description">`
   - Open Graph tags (`og:title`, `og:description`, etc.)
   - Twitter Card tags

2. **Structured Data**: Look for `<script type="application/ld+json">` tags

3. **Sitemap**: Visit `https://yourdomain.com/sitemap.xml`

4. **robots.txt**: Visit `https://yourdomain.com/robots.txt`

## 🚀 Next Steps

1. ✅ Set your `url` in `_config.yml`
2. ✅ Add excerpts to existing posts
3. ✅ Add alt text to images
4. ✅ Submit sitemap to Google Search Console
5. ✅ Monitor performance and iterate

## 📚 Resources

- [Jekyll SEO Tag Documentation](https://github.com/jekyll/jekyll-seo-tag)
- [Google Search Central](https://developers.google.com/search)
- [Schema.org Documentation](https://schema.org/)

