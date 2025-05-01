# CrewFox Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the CrewFox landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Navigation Links](#managing-navigation-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Main Sections Overview
The landing page consists of these key sections:
- Header (Navigation)
- Hero Section
- Services Section
- Benefits Section
- FAQ Section
- Contact Section
- Footer

### Updating Text Content

#### Hero Section
```html
<!-- Located in the first section after <main> -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8">
    TAKE YOUR BUSINESS TO THE NEXT LEVEL WITH OUR SERVICES
</h1>
```
To modify the main headline:
1. Locate the `<h1>` tag in the hero section
2. Replace the text between the opening and closing tags
3. Maintain the CAPS style if desired

#### Services Cards
```html
<!-- Located in the services section -->
<div class="bg-gray-900 rounded-2xl p-8 hover:transform hover:scale-105 transition-all duration-300">
    <h3 class="text-2xl font-bold mb-4">CrewFox IT</h3>
    <p class="text-gray-300">Comprehensive IT solutions tailored to your business needs</p>
</div>
```
To update service descriptions:
1. Find the service cards in the `#services` section
2. Modify the text within the `<h3>` and `<p>` tags
3. Keep descriptions concise and clear

### Modifying Tailwind CSS Classes

#### Understanding Key Classes
- `container mx-auto px-6`: Centers content with padding
- `grid grid-cols-1 md:grid-cols-2`: Creates responsive grid layout
- `text-gray-300`: Sets text color
- `hover:transform hover:scale-105`: Adds hover animation

#### Example: Changing Colors
To change text color from gray to white:
```html
<!-- Original -->
<p class="text-gray-300">Your text here</p>

<!-- Modified -->
<p class="text-white">Your text here</p>
```

#### Example: Adjusting Spacing
To modify padding:
```html
<!-- Original -->
<div class="p-8">Content</div>

<!-- Modified -->
<div class="p-4">Content</div> <!-- Less padding -->
```

## Managing Navigation Links

### Current Navigation Structure
```html
<div class="hidden md:flex space-x-8">
    <a href="#services" class="text-gray-300 hover:text-white transition-colors duration-300">Services</a>
    <a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
    <a href="#faq" class="text-gray-300 hover:text-white transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-300 hover:text-white transition-colors duration-300">Contact</a>
</div>
```

### Updating Navigation Links
1. Locate the navigation div in the header
2. Update the `href` attribute to match your section IDs
3. Modify the link text between the `<a>` tags

Example:
```html
<!-- To add a new link -->
<a href="#new-section" class="text-gray-300 hover:text-white transition-colors duration-300">New Section</a>
```

### External Links
For external links (like email):
```html
<!-- Example from contact section -->
<a href="mailto:john@crewfoxx.com" class="inline-block bg-white text-gray-900 px-8 py-4 rounded-lg font-semibold">
    Contact Us
</a>
```

## Adding Privacy and Terms Pages

### Current Footer Links
```html
<div class="space-y-2">
    <a href="#" class="block text-gray-300 hover:text-white transition-colors duration-300">Privacy Policy</a>
    <a href="#" class="block text-gray-300 hover:text-white transition-colors duration-300">Terms of Service</a>
</div>
```

### Steps to Add Policy Pages
1. Create new HTML files:
   - `privacy.html`
   - `terms.html`

2. Update the footer links:
```html
<div class="space-y-2">
    <a href="privacy.html" class="block text-gray-300 hover:text-white transition-colors duration-300">Privacy Policy</a>
    <a href="terms.html" class="block text-gray-300 hover:text-white transition-colors duration-300">Terms of Service</a>
</div>
```

3. Ensure consistent styling by copying the header and footer from index.html to your new pages

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Check that section IDs match href attributes
   - Ensure IDs are unique
   - Example: `href="#services"` should match `id="services"`

2. **Responsive Design Issues**
   - Verify media query classes (md:, lg:) are correctly placed
   - Test on different screen sizes
   - Example: `class="hidden md:flex"` hides on mobile, shows on medium screens

3. **Style Inconsistencies**
   - Keep Tailwind classes consistent across similar elements
   - Copy existing classes for new elements
   - Example: Use `text-gray-300 hover:text-white transition-colors duration-300` for all navigation links

### Need Help?
- Double-check your changes against the original code
- Use browser developer tools (F12) to inspect elements
- Ensure all HTML tags are properly closed
- Verify file paths for new pages are correct

Remember to test all changes across different devices and browsers before publishing updates to your live site.