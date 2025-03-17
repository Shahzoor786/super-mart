# LuxeVibe - Developer Documentation

This document provides technical information for developers who want to customize or extend the LuxeVibe e-commerce template.

## Technical Architecture

The LuxeVibe template follows a simple, modular architecture:

- **HTML**: Semantic markup with clear section divisions
- **CSS**: Modular CSS with variables for easy customization
- **JavaScript**: Vanilla JavaScript with minimal dependencies

## CSS Architecture

The CSS is organized using a component-based approach:

1. **Variables**: Global variables defined in the `:root` selector for colors, shadows, transitions, etc.
2. **Base Styles**: Reset and basic element styling
3. **Components**: Each major UI component has its own section (navbar, hero, products, etc.)
4. **Utilities**: Helper classes and animations
5. **Responsive**: Media queries in a separate file

### CSS Variables

All theme colors and common properties are defined as CSS variables. To change the theme, modify these variables in the `:root` section of `styles.css`:

```css
:root {
    --primary-color: #3498db;
    --secondary-color: #2ecc71;
    --dark-color: #2c3e50;
    --light-color: #f8f9fa;
    --text-color: #333;
    --sale-color-1: #ff416c;
    --sale-color-2: #ff4b2b;
    --accent-color: #ffd700;
    /* ...other variables... */
}
```

## JavaScript Components

### 1. Product Slider

The product slider uses Swiper.js. Configuration options:

```javascript
const swiper = new Swiper('.product-slider', {
    slidesPerView: 1,
    spaceBetween: 30,
    loop: true,
    pagination: {
        el: '.swiper-pagination',
        clickable: true,
    },
    navigation: {
        nextEl: '.swiper-button-next',
        prevEl: '.swiper-button-prev',
    },
    breakpoints: {
        640: {
            slidesPerView: 2,
        },
        968: {
            slidesPerView: 3,
        },
    },
});
```

### 2. Mobile Menu

The mobile menu toggle functionality:

```javascript
const hamburger = document.querySelector('.hamburger');
const navLinks = document.querySelector('.nav-links');
const navIcons = document.querySelector('.nav-icons');

hamburger.addEventListener('click', () => {
    navLinks.classList.toggle('active');
    navIcons.classList.toggle('active');
    hamburger.classList.toggle('active');
});
```

### 3. Contact Form

The contact form uses AJAX for submission. To configure the form endpoint, modify the `formSubmit` function in `script.js`.

## Adding New Pages

To add new pages:

1. Create a new HTML file using `index.html` as a template
2. Update navigation links in each file to point to the new page
3. Maintain the same header and footer structure

## Performance Optimization

The template is optimized for performance with:

- Minified external libraries
- Optimized images (using `width` and `height` attributes)
- Lazy loading for images (add `loading="lazy"` to images below the fold)
- Efficient CSS selectors
- Minimal JavaScript

## Browser Support

The template is designed to work on modern browsers (last 2 versions):
- Chrome
- Firefox
- Safari
- Edge
- Opera

## Third-Party Libraries

1. **Swiper.js**: For the product carousel
2. **Font Awesome**: For icons
3. **Google Fonts (Poppins)**: For typography

## Customization Checklist

When customizing this template for a project:

1. Update favicon
2. Modify color scheme (CSS variables)
3. Replace images with project-specific ones
4. Update product information
5. Configure contact form endpoint
6. Customize footer links and information
7. Add analytics (Google Analytics or similar)
8. Test responsiveness on various devices

## Build Process (Optional)

For production:

1. Minify CSS
2. Minify JavaScript
3. Optimize images
4. Enable gzip compression on server

## Support and Resources

- [Swiper Documentation](https://swiperjs.com/get-started)
- [Font Awesome Icons](https://fontawesome.com/icons)
- [Google Fonts](https://fonts.google.com/)
- [Unsplash](https://unsplash.com/) (for royalty-free images) 