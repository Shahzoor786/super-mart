# LuxeVibe - Premium E-Commerce Template

A modern, responsive e-commerce website template built with HTML, CSS, and vanilla JavaScript.

![LuxeVibe Preview](assets/images/preview.jpg)

## Features

- **Responsive Design**: Fully responsive design that looks great on all devices
- **Modern UI/UX**: Clean and modern user interface with smooth animations
- **Product Carousel**: Interactive product slider using Swiper.js
- **Sale Section**: Eye-catching sale section with animations and discount badges
- **Category Grid**: Visual category navigation with hover effects
- **Contact Form**: AJAX-powered contact form with validation
- **Animated Navigation**: Smooth animations for navigation elements
- **CSS Animations**: Various animations throughout the site for enhanced user experience
- **Cross-Browser Compatible**: Tested across major browsers

## Getting Started

### Prerequisites

- A code editor (VS Code, Sublime Text, etc.)
- Basic knowledge of HTML, CSS, and JavaScript

### Installation

1. Download or clone this repository
2. Open the project in your code editor
3. Customize the content to fit your needs

## File Structure

```
luxevibe/
├── index.html              # Main HTML file
├── assets/
│   ├── css/
│   │   ├── styles.css      # Main CSS file
│   │   └── responsive.css  # Responsive styles
│   ├── js/
│   │   └── script.js       # Main JavaScript file
│   ├── images/             # Image files
│   └── fonts/              # Custom fonts (if any)
├── favicon.ico             # Favicon
└── README.md               # Documentation
```

## Customization

### Changing Colors

The template uses CSS variables for colors. You can modify them in the `:root` section in `styles.css`:

```css
:root {
  --primary-color: #3498db;
  --secondary-color: #2ecc71;
  --dark-color: #2c3e50;
  --light-color: #f8f9fa;
  --sale-color-1: #ff416c;
  --sale-color-2: #ff4b2b;
  --accent-color: #ffd700;
}
```

### Adding Products

To add more products to the featured section, duplicate the product card structure in `index.html`:

```html
<div class="swiper-slide product-card">
    <img src="path/to/image.jpg" alt="Product Name">
    <h3>Product Name</h3>
    <p class="price">$199.99</p>
    <button class="add-to-cart">Add to Cart</button>
</div>
```

### Modifying the Sale Section

Update the sale items by changing the content in the sale section:

```html
<div class="sale-item">
    <span class="discount-badge">-40%</span>
    <img src="path/to/image.jpg" alt="Product Name">
    <h3>Product Name</h3>
    <div class="price-tag">
        <span class="original-price">$299.99</span>
        <span class="sale-price">$179.99</span>
    </div>
    <a href="#" class="sale-button">Shop Now</a>
</div>
```

## Dependencies

- [Font Awesome](https://fontawesome.com/) - For icons
- [Google Fonts (Poppins)](https://fonts.google.com/specimen/Poppins) - For typography
- [Swiper.js](https://swiperjs.com/) - For the product carousel

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Opera (latest)

## License

This template is released under the MIT License. See the LICENSE file for details.

## Acknowledgments

- Images from [Unsplash](https://unsplash.com/)
- Icons from [Font Awesome](https://fontawesome.com/)
- Inspired by modern e-commerce design trends 