# GitHub Pages + Jekyll Template Guide

This guide explains the structure of this Jekyll template and teaches you Markdown syntax to use throughout the site.

## Table of Contents

1. [Template Structure](#template-structure)
2. [Key Files Explained](#key-files-explained)
3. [Folders Explained](#folders-explained)
4. [Markdown Basics](#markdown-basics)
5. [Writing Posts](#writing-posts)
6. [Writing Pages](#writing-pages)

---

## Template Structure

This is a Jekyll-based GitHub Pages site using the **Minimal Mistakes** theme. Jekyll is a static site generator that converts Markdown files into a complete website.

### How It Works

1. You write content in Markdown files
2. Jekyll processes these files and converts them to HTML
3. GitHub Pages hosts the resulting website automatically
4. The Minimal Mistakes theme provides the styling and layout

---

## Key Files Explained

### `_config.yml`

This is the **main configuration file** for your Jekyll site. It controls:

- **Site metadata**: Title, email, description
- **Social links**: Twitter, GitHub, Instagram handles
- **Theme settings**: Which theme to use (Minimal Mistakes)
- **Plugins**: Additional Jekyll functionality
- **Author information**: Your name, bio, and profile picture
- **Default layouts**: How posts and pages are displayed

**Example**: The line `title: MM` sets your site's title. Change this to your site's name.

### `Gemfile`

Lists all Ruby dependencies (libraries) your site needs. This ensures the site builds consistently.

### `index.html`

The homepage of your site. This is what visitors see first.

### `README.md`

Documentation for your repository. GitHub displays this on your repo's main page.

### `Gemfile.lock`

Auto-generated file that locks specific versions of dependencies. Don't edit this manually.

---

## Folders Explained

### `_config.yml` (root level)

Stores site configuration (described above).

### `_data/`

Contains YAML data files for site-wide information. For example:
- `navigation.yml` defines your site's navigation menu

### `_pages/`

Stores static pages that appear on your site:
- **404.md**: Custom 404 "page not found" error
- **about.md**: About page
- **category-archive.md**: Shows all posts by category
- **tag-archive.md**: Shows all posts by tag
- **year-archive.md**: Shows all posts by year

### `_posts/`

**Your blog posts go here.** Each file must be named following this pattern:

```
YYYY-MM-DD-post-title.md
```

Example: `2024-01-15-my-first-post.md`

### `assets/`

Stores static files that don't change:
- `images/`: Store your images here

---

## Markdown Basics

Markdown is a lightweight markup language that's easy to read and write. Here are the essential syntax elements:

### Headings

```markdown
# Heading 1 (Largest)
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6 (Smallest)
```

**Result**: Creates hierarchical headings. Use `#` for main title, `##` for sections, etc.

### Emphasis

```markdown
*Italic text* or _Italic text_
**Bold text** or __Bold text__
***Bold and italic*** or ___Bold and italic___
~~Strikethrough~~ (if supported)
```

**Result**: 
- *Italic text*
- **Bold text**
- ***Bold and italic***
- ~~Strikethrough~~

### Lists

#### Unordered Lists

```markdown
- Item 1
- Item 2
  - Nested item 2.1
  - Nested item 2.2
- Item 3
```

**Result**:
- Item 1
- Item 2
  - Nested item 2.1
  - Nested item 2.2
- Item 3

#### Ordered Lists

```markdown
1. First item
2. Second item
3. Third item
   1. Nested item 3.1
   2. Nested item 3.2
```

**Result**:
1. First item
2. Second item
3. Third item
   1. Nested item 3.1
   2. Nested item 3.2

### Links

```markdown
[Link text](https://example.com)
[Link with title](https://example.com "Hover text")
```

**Result**: Creates clickable links. The text in square brackets is what displays; the URL is in parentheses.

### Images

```markdown
![Alt text](./assets/images/my-image.jpg)
![Alt with link](./assets/images/photo.jpg "Caption")
```

**Result**: Displays an image. Alt text appears if the image can't load. Use relative paths starting with `./`.

### Code

#### Inline Code

```markdown
Use `variable_name` or `function()` for inline code.
```

**Result**: Use `variable_name` or `function()` for inline code.

#### Code Blocks

Use triple backticks with optional language:

````markdown
```python
def hello_world():
    print("Hello, World!")
```
````

```python
def hello_world():
    print("Hello, World!")
```

### Blockquotes

```markdown
> This is a quote.
> It can span multiple lines.

> **Nested quotes**
> > This is a nested quote
```

**Result**:
> This is a quote.
> It can span multiple lines.

> **Nested quotes**
> > This is a nested quote

### Horizontal Rules

```markdown
---
or
***
or
___
```

**Result**: Creates a horizontal line.

### Tables

```markdown
| Header 1 | Header 2 | Header 3 |
|----------|----------|----------|
| Cell 1   | Cell 2   | Cell 3   |
| Cell 4   | Cell 5   | Cell 6   |
```

**Result**:

| Header 1 | Header 2 | Header 3 |
|----------|----------|----------|
| Cell 1   | Cell 2   | Cell 3   |
| Cell 4   | Cell 5   | Cell 6   |

### Escaping Characters

Use a backslash to display special characters literally:

```markdown
\*Not italic\*
\[Not a link\]
```

---

## Writing Posts

Posts are the main content of your blog. Here's how to create one:

### File Naming

Save files in `_posts/` with this format:
```
YYYY-MM-DD-title-of-post.md
```

Example: `2024-01-15-my-awesome-post.md`

### Front Matter

Every post starts with **front matter** (YAML between `---` markers):

```markdown
---
title: "My First Blog Post"
date: 2024-01-15
categories: [learning, jekyll]
tags: [markdown, github-pages]
author_profile: true
read_time: true
comments: true
share: true
related: true
---

# Your post content starts here

You can write your post in Markdown...
```

**Common front matter fields**:
- `title`: Post title
- `date`: Publication date (YYYY-MM-DD format)
- `categories`: Category/categories for organizing posts
- `tags`: Tags for organizing posts
- `layout`: Post layout (usually `single`)
- `author_profile`: Show author info (true/false)
- `read_time`: Show estimated reading time (true/false)
- `comments`: Enable comments (true/false)

### Example Post

```markdown
---
title: "Learning Markdown"
date: 2024-01-15
categories: [tutorial]
tags: [markdown, writing]
---

# Learning Markdown

This is my first post about Markdown!

## Why Markdown?

Markdown is **easy** to write and **readable** as plain text.

## My Favorite Features

1. Simple syntax
2. Converts to HTML automatically
3. Perfect for blogging

Check out [the Markdown guide](https://www.markdownguide.org) for more info.
```

---

## Writing Pages

Pages are like posts but don't appear in your blog feed. Use them for permanent content like "About Me."

### File Naming

Save files in `_pages/` with any name:
```
about.md
portfolio.md
contact.md
```

### Front Matter for Pages

```markdown
---
title: "About Me"
permalink: /about/
layout: single
author_profile: true
---

# About Me

Tell visitors about yourself here...
```

**Key differences from posts**:
- No date required
- Use `permalink` to set the URL
- Usually `layout: single`
- Appears in navigation menu (if added to `navigation.yml`)

---

## Useful Tips

### Adding Images to Posts

1. Save your image in `assets/images/`
2. Reference it in your post:

```markdown
![My image description](../assets/images/my-image.jpg)
```

### Creating a Table of Contents

Use this at the top of long posts:

```markdown
## Table of Contents
1. [Section One](#section-one)
2. [Section Two](#section-two)
3. [Section Three](#section-three)

## Section One

Content here...

## Section Two

Content here...

## Section Three

Content here...
```

### Publishing Your Site

Once you push changes to GitHub:
1. GitHub automatically builds your site
2. It appears at `https://username.github.io/daah/` (or your custom domain)
3. Changes usually appear within a few minutes

### Local Testing

To test your site before publishing:

```bash
bundle install
bundle exec jekyll serve
```

Then visit `http://localhost:4000`

---

## Next Steps

1. Update `_config.yml` with your site information
2. Edit `_pages/about.md` to tell your story
3. Create your first post in `_posts/`
4. Push to GitHub to see your site live!

Happy writing!
