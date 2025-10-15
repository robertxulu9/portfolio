# WARP.md

This file provides guidance to WARP (warp.dev) when working with code in this repository.

## Project Overview

This is Zulu Robert's personal portfolio website built as a single-page application using HTML5, CSS3, JavaScript, and Bootstrap. The site showcases professional experience as a Full Stack Developer and IT Technician with sections for About, Skills, Services, Projects, and Contact information.

## Architecture & Structure

### Frontend Stack
- **HTML5**: Single-page application with semantic markup (`index.html`)
- **CSS3**: Custom styles in `css/style.css` with CSS variables for theming
- **Bootstrap 5**: UI framework loaded via CDN with custom SCSS variables
- **JavaScript**: jQuery-based interactions in `js/main.js`
- **Third-party Libraries**:
  - WOW.js for scroll animations
  - Typed.js for typing effect animations  
  - Owl Carousel for testimonial carousels
  - Isotope for portfolio filtering
  - Lightbox for image galleries
  - CounterUp for animated statistics

### Directory Structure
```
portfolio/
├── index.html          # Main HTML file
├── css/               # Stylesheets
│   ├── style.css      # Custom CSS with CSS variables
│   └── bootstrap.min.css
├── scss/              # SCSS source files
│   ├── bootstrap.scss # Bootstrap customization
│   └── bootstrap/     # Bootstrap SCSS framework
├── js/                # JavaScript files
│   └── main.js        # Main application logic
├── lib/               # Third-party libraries
├── img/               # Images and graphics
└── documents/         # PDF documents (certificates, CV, etc.)
```

### Key Components
- **Responsive Design**: Mobile-first approach with Bootstrap grid system
- **Smooth Scrolling**: Single-page navigation with animated scrolling
- **Dynamic Content**: Typed animations, counter animations, progress bars
- **Interactive Portfolio**: Filterable project gallery with lightbox
- **Contact Integration**: Direct phone and email links

## Development Commands

### Serving the Website
Since this is a static website, serve it using any HTTP server:
```bash
# Using Python (if available)
python -m http.server 8000

# Using Node.js (if available)
npx serve .

# Using PHP (if available)
php -S localhost:8000
```

### SCSS Compilation
If modifying SCSS files, compile using:
```bash
# Using Sass CLI (if available)
sass scss/bootstrap.scss css/bootstrap.min.css --style compressed
```

### File Operations
- **Static Assets**: All images go in `img/` directory
- **Documents**: PDF files in `documents/` directory
- **Fonts**: Loaded via Google Fonts CDN
- **Icons**: Font Awesome 5 and Bootstrap Icons via CDN

## Development Guidelines

### CSS Customization
- Primary theme colors defined in CSS variables in `:root`
- Custom Bootstrap variables in `scss/bootstrap.scss`
- Follow existing naming conventions for CSS classes

### JavaScript Modifications
- All custom JS in `js/main.js` using jQuery
- Libraries loaded from `lib/` directory
- Event handlers follow jQuery patterns with IIFE wrapper

### Content Updates
- Personal information in HTML sections with semantic IDs
- Project showcase in portfolio section with lightbox integration
- Skills progress bars with `aria-valuenow` attributes
- Contact details in footer section

### Image Optimization
- Profile images should be optimized for web
- Project thumbnails should maintain consistent aspect ratios
- Use appropriate image formats (JPG for photos, PNG for graphics)

## Browser Support

The site targets modern browsers with:
- Bootstrap 5 compatibility
- ES5+ JavaScript features
- CSS3 animations and transitions
- Responsive design breakpoints

## Deployment

This is a static website that can be deployed to:
- GitHub Pages
- Netlify
- Vercel
- Any web hosting service

No build process required - files can be uploaded directly to web server.