# Texas Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web Design landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains your logo and navigation menu. To update:

1. **Logo Text:**
```html
<!-- Find this line in the header section -->
<div class="text-2xl font-bold text-blue-600">TWD</div>
```
Simply replace "TWD" with your desired text.

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```
Replace the text between `<a>` tags to change menu items.

### Hero Section
Update the main headline and subheading:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">
    Texas Web Design
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12 leading-relaxed">
    Best Websites In Texas
</p>
```

### Tailwind CSS Classes Explained
Common classes used throughout:
- `text-[size]`: Controls text size (xl, 2xl, 3xl, etc.)
- `font-[weight]`: Controls text weight (bold, semibold, etc.)
- `bg-[color]`: Sets background color
- `text-[color]`: Sets text color
- `p-[size]`: Sets padding
- `m-[size]`: Sets margin
- `rounded-[size]`: Controls border radius

Example of modifying a button:
```html
<!-- Original -->
<a href="https://twd.com" class="bg-blue-600 text-white px-8 py-4 rounded-full">

<!-- Modified for different color and size -->
<a href="https://twd.com" class="bg-green-600 text-white px-6 py-3 rounded-lg">
```

## Fixing Broken Links

### Current Link Inventory
1. Navigation Menu Links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

2. Call-to-Action Links:
```html
<a href="https://twd.com" class="bg-blue-600">Get Started</a>
```

### Updating Links
1. For internal section links (starting with #):
   - Ensure the href matches the id of the target section
   - Example: `href="#features"` should match `id="features"`

2. For external links:
   - Replace `https://twd.com` with your actual website URL
   - Example:
```html
<!-- Before -->
<a href="https://twd.com">Get Started</a>

<!-- After -->
<a href="https://your-actual-domain.com">Get Started</a>
```

## Linking Privacy and Terms Pages

### Footer Links Setup
Locate the legal section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link to privacy and terms pages:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Check that section IDs match href attributes exactly
   - IDs are case-sensitive
   - Example: `href="#FAQ"` won't link to `id="faq"`

2. **Responsive Design Issues**
   - Classes starting with `md:` only apply on medium screens and up
   - Classes starting with `lg:` only apply on large screens and up
   - If mobile layout looks wrong, check the base classes (without md: or lg: prefixes)

3. **Missing Styles**
   - Verify the Tailwind CSS CDN link is working
   - Check for typos in class names
   - Tailwind classes must be exact matches

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate your HTML at [W3C Validator](https://validator.w3.org/)
- Test responsive design using browser developer tools

Remember to always backup your files before making changes, and test thoroughly across different devices and browsers after updates.