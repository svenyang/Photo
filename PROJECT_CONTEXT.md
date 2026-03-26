# Project Context Analysis: PhotoBlog

## 1. Core Directory Structure

```
PhotoBlog/
├── assets/                 # Frontend assets (CSS, JS)
│   ├── css/
│   │   ├── _colors.scss
│   │   ├── _normalize.scss
│   │   ├── _styles.scss
│   │   ├── custom.css
│   │   ├── main.scss
│   │   └── photoswipe/     # PhotoSwipe lightbox library
│   └── js/                 # JavaScript files
│       ├── gallery.js
│       ├── lazysizes.js
│       ├── lightbox.js
│       ├── main.js
│       ├── menu.js
│       ├── justified-layout/
│       └── photoswipe/
├── content/                # Markdown content with photos
│   ├── _index.md
│   ├── index.md
│   ├── neimenggu/          # Example photo album
│   │   ├── index.md
│   │   └── neimenggu.json
│   └── tianehubj/          # Another example photo album
│       ├── index.md
│       └── tianehubj.json
├── layouts/                # Hugo templates
│   ├── _default/
│   └── partials/           # Reusable template components
├── i18n/                   # Internationalization files
├── static/                 # Static assets
├── public/                 # Generated site (build output)
├── config.yaml             # Site configuration
├── hugo.toml               # Hugo configuration
├── theme.toml              # Theme metadata
├── package.json            # Node.js dependencies
├── README.md               # Project documentation
└── exampleSite/            # Example site with sample content
```

## 2. Technology Stack

- **Framework**: Hugo (Static Site Generator)
- **Language**: Go templating (HTML templates with Hugo functions)
- **Frontend**: 
  - CSS/SCSS for styling
  - JavaScript for interactivity
  - PhotoSwipe for lightbox functionality
  - Justified Layout (Flickr's algorithm) for photo arrangement
- **Build Tool**: Hugo Extended (required for asset processing)
- **Version Control**: Git
- **Package Manager**: Go modules (for Hugo modules)

## 3. Key Dependencies

- **Hugo Extended** >= 0.121.2 (required for asset pipeline)
- **PhotoSwipe** - JavaScript library for lightbox functionality
- **Justified Layout** - Flickr's algorithm for arranging photos
- **LazySizes** - Lazy loading for images
- **Go modules** - Dependency management

## 4. Entry Points & Main Files

- **hugo.toml** - Main Hugo configuration file
- **theme.toml** - Theme metadata
- **content/index.md** - Homepage content
- **layouts/_default/baseof.html** - Base HTML template
- **layouts/_default/list.html** - Template for album lists
- **layouts/_default/single.html** - Template for individual galleries
- **layouts/partials/gallery.html** - Gallery rendering logic
- **layouts/partials/get-gallery.html** - Gallery data processing
- **assets/js/gallery.js** - JavaScript for gallery functionality
- **assets/js/lightbox.js** - PhotoSwipe integration
- **assets/css/main.scss** - Main stylesheet

## 5. Project Functionality

This is a photo gallery theme for Hugo that:

- Collects photos from markdown content files and their associated image resources
- Creates hierarchical album structures based on folder organization
- Generates responsive galleries with justified layout
- Provides lightbox functionality with PhotoSwipe
- Supports both local images and remote image URLs (via JSON files)
- Includes dark/light theme options
- Offers lazy loading for performance
- Provides SEO features with Open Graph tags

## 6. Content Organization

The site organizes content hierarchically:
- Top-level folders in `content/` represent main albums
- Subfolders represent sub-albums
- Images within folders are collected and displayed in galleries
- JSON files can be used to include remote images
- Frontmatter in markdown files controls album properties (title, date, privacy, etc.)

## 7. Key Features

- Responsive design with mobile-friendly layout
- Justified photo layout algorithm (like Flickr)
- Lightbox viewing with zoom and navigation
- Support for EXIF metadata (titles from ImageDescription)
- Private albums (hidden from public listings)
- Featured album highlighting
- Multi-language support (i18n)
- Lazy loading for improved performance
- SEO optimization with structured data