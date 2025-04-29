# Texas Web Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web landing page. It's written for beginners and provides step-by-step instructions for common updates.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Legal Pages](#adding-legal-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Key Sections for Text Updates

#### Header (Company Name)
```html
<a href="/" class="text-2xl font-bold text-blue-600">Texas Web</a>
```
To change the company name, modify the text between the `<a>` tags.

#### Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">
    Best Websites In Texas
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">{hero_statement}</p>
```
- Replace `Best Websites In Texas` with your main headline
- Replace `{hero_statement}` with your subheading text

#### Features Cards
Each feature card follows this structure:
```html
<div class="bg-white rounded-xl p-8 shadow-lg hover:shadow-xl transition-shadow duration-300">
    <h3 class="text-xl font-semibold mb-4">Easy to Use</h3>
    <p class="text-gray-600 leading-relaxed">Intuitive interface and user-friendly design...</p>
</div>
```
To update:
1. Locate the feature card you want to change
2. Modify the `<h3>` text for the title
3. Update the `<p>` text for the description

### Understanding Tailwind Classes

Key class combinations used in this template:

```css
/* Container width and padding */
container mx-auto px-6

/* Text sizes and colors */
text-4xl (large text)
text-gray-600 (gray text)
text-blue-600 (blue text)

/* Spacing */
mb-6 (margin bottom)
py-24 (padding top and bottom)

/* Responsive design */
md:text-5xl (applies at medium screens)
lg:text-6xl (applies at large screens)
```

To modify styles:
1. Find the element you want to change
2. Reference the [Tailwind CSS documentation](https://tailwindcss.com/docs)
3. Replace or add classes while maintaining the responsive prefixes (md:, lg:)

## Managing Links

### Navigation Menu Links
Current navigation structure:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update internal links:
1. Identify the section ID you want to link to
2. Update the `href` attribute with `#section-id`
3. Ensure the target section has a matching `id` attribute

### Call-to-Action Links
Current CTA buttons point to "https://sigmaseo.io":
```html
<a href="https://sigmaseo.io" class="inline-block px-8 py-4 bg-blue-600...">
```

To update:
1. Locate all instances of `https://sigmaseo.io`
2. Replace with your desired URL
3. Test all buttons to ensure they work

## Adding Legal Pages

### Footer Legal Links
Current structure:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add privacy and terms pages:
1. Create new files:
   - `privacy.html`
   - `terms.html`
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match exactly with href attributes
   - IDs are case-sensitive
   - Check for extra spaces in IDs

2. **Responsive Design Issues**
   - Keep the `md:` and `lg:` prefixes when modifying classes
   - Test on multiple screen sizes
   - Don't remove the `container` class from main sections

3. **Missing Styles**
   - Verify the Tailwind CDN link is present in the head section
   - Check for typos in class names
   - Ensure all closing tags are present

### Need Help?

If you encounter issues:
1. Check the browser console for errors
2. Verify all files are in the correct directory
3. Double-check class names against the Tailwind documentation
4. Ensure all HTML tags are properly closed

Remember to always make a backup of your files before making changes!