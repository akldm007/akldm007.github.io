# SeanLi's Blog

A modern, responsive blog built with Jekyll featuring a clean 2025 design aesthetic.

## 🎨 Design Features

### Modern 2025 Design Trends
- **Clean Minimalist Layout**: Focused on content readability with generous whitespace
- **Modern Color Palette**: Indigo and purple gradient accents (#6366f1, #8b5cf6)
- **System Fonts**: Native font stack for optimal performance and native feel
- **Smooth Animations**: Subtle transitions and hover effects throughout
- **Glass Morphism**: Frosted glass effect on sticky header
- **Card-Based Design**: Elevated cards with shadows for content sections

### Dark Mode Support
- **Auto-Detection**: Respects system preference automatically
- **Manual Toggle**: Beautiful animated sun/moon icon toggle in header
- **Persistent Choice**: Remembers user preference via localStorage
- **Seamless Transitions**: Smooth color transitions when switching themes

### Typography
- **Modern Font Stack**: Inter, SF Pro, system fonts for crisp rendering
- **Optimal Line Height**: 1.7 for comfortable reading
- **Responsive Sizes**: Fluid typography that scales beautifully
- **Code Highlighting**: JetBrains Mono with Fira Code fallback

### Responsive Design
- **Mobile-First**: Optimized for all screen sizes
- **Sticky Navigation**: Header stays accessible while scrolling
- **Grid Layouts**: Modern CSS Grid for flexible layouts
- **Touch-Friendly**: Large tap targets and proper spacing

### Performance
- **Optimized Assets**: Efficient CSS with minimal overhead
- **No External Dependencies**: Self-contained design system
- **Fast Loading**: Minimal JavaScript, CSS-driven animations
- **SEO Optimized**: Proper meta tags and semantic HTML

## 🚀 Getting Started

### Prerequisites
- Ruby 2.7 or higher
- Jekyll 4.0 or higher
- Bundler

### Local Development

1. Clone the repository:
```bash
git clone https://github.com/akldm007/akldm007.github.io.git
cd akldm007.github.io
```

2. Install dependencies:
```bash
bundle install
```

3. Run the development server:
```bash
bundle exec jekyll serve
```

4. Open your browser and visit:
```
http://localhost:4000
```

### Deployment

This blog is designed to be deployed on GitHub Pages. Simply push your changes to the `main` branch:

```bash
git add .
git commit -m "Update blog"
git push origin main
```

GitHub Pages will automatically build and deploy your site.

## 📝 Creating Posts

Create a new file in the `_posts` directory with the format:
```
YYYY-MM-DD-title.markdown
```

Example post structure:
```markdown
---
layout: post
title: "Your Post Title"
date: 2025-01-27
categories: [category1, category2]
---

Your content here...
```

## 🎨 Customization

### Colors
Edit `css/main.scss` to customize the color scheme:
```scss
$primary-color: #6366f1;  // Main brand color
$accent-color: #8b5cf6;   // Secondary accent
```

### Site Information
Update `_config.yml` with your information:
```yaml
title: Your Blog Name
author: Your Name
email: your.email@example.com
description: Your blog description
```

### Avatar
Replace `/pic/jm.jpg` with your own avatar image.

## 📁 Project Structure

```
akldm007.github.io/
├── _includes/          # Reusable components
│   ├── head.html      # HTML head with meta tags
│   ├── header.html    # Site header with navigation
│   ├── footer.html    # Site footer
│   └── sidebar.html   # Sidebar content
├── _layouts/          # Page templates
│   ├── default.html   # Base layout
│   ├── post.html      # Blog post layout
│   └── page.html      # Static page layout
├── _posts/            # Blog posts
├── _sass/             # SCSS stylesheets
│   ├── _base.scss     # Base styles & typography
│   ├── _layout.scss   # Layout components
│   ├── _home.scss     # Home page styles
│   └── _post.scss     # Post page styles
├── css/
│   └── main.scss      # Main stylesheet (imports partials)
├── _config.yml        # Jekyll configuration
└── index.html         # Homepage

```

## 🌟 Key Features

- **Gradient Headings**: Eye-catching gradient text on titles
- **Hover Animations**: Smooth transitions on interactive elements
- **Modern Pagination**: Clean navigation between pages
- **Card Hover Effects**: Subtle lift and shadow on hover
- **Responsive Images**: Automatic scaling with border radius
- **Code Syntax Highlighting**: Beautiful code blocks with Rouge
- **SEO Optimized**: Open Graph and Twitter Card meta tags
- **RSS Feed**: Built-in feed for subscribers

## 📱 Browser Support

- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- Built with [Jekyll](https://jekyllrb.com/)
- Hosted on [GitHub Pages](https://pages.github.com/)
- Icons from SVG icon libraries
- Inspired by modern web design trends of 2025

---

**Note**: This is a modernized version of the blog with 2025 design trends including dark mode, smooth animations, modern typography, and a clean aesthetic focused on readability and user experience.
