# BocceCourtHub Landing Page - Maintenance Guide

This guide will help you maintain and customize the BocceCourtHub landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text:**
```html
<!-- Find this section in the header -->
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">
    BocceCourt<span class="text-white">Hub</span>
</a>
```
- Change "BocceCourt" or "Hub" by editing the text directly
- Keep the `<span>` tag to maintain the two-tone effect

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-300 hover:text-white transition duration-300">Features</a>
    <a href="#benefits" class="text-gray-300 hover:text-white transition duration-300">Benefits</a>
    <a href="#contact" class="text-gray-300 hover:text-white transition duration-300">Contact</a>
</div>
```
- Edit text between `<a>` tags to change menu items
- Keep the `class` attributes unchanged to maintain styling

### Hero Section
The main headline and introduction are in the hero section:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent">
    Build the Perfect Bocce Ball Court
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    Create a flawless bocce court with expert tips & guides!
</p>
```
- Update headline text between the `<h1>` tags
- Modify subtitle text between the `<p>` tags
- Keep responsive classes (`text-4xl md:text-5xl lg:text-6xl`) to maintain proper sizing across devices

### Understanding Key Tailwind Classes
- `text-{size}`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `md:` or `lg:`: Applies styles at specific breakpoints
- `mb-{size}`: Adds margin bottom (e.g., `mb-8`, `mb-12`)
- `bg-gradient-to-r`: Creates right-flowing gradient
- `hover:scale-105`: Enlarges element on hover

## Fixing Broken Links

### Navigation Links
Current internal links in the navigation:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#contact">Contact</a>
```

To update:
1. Internal links (same page):
   - Keep the `#` symbol
   - Match the `id` of the target section
   - Example: `href="#features"` jumps to `<section id="features">`

2. External links:
   - Replace `#` with full URL
   - Example: `href="https://example.com/features"`

### Call-to-Action Buttons
Update the main CTA links:
```html
<a href="https://boccecourthub.com" class="inline-block bg-gradient-to-r...">
    Start Your Court Project
</a>
```
- Replace `https://boccecourthub.com` with your desired URL
- Test links after updating to ensure they work

## Linking Privacy and Terms Pages

### Footer Legal Links
Current placeholder links:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create privacy.html and terms.html files in your project
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Gradients**
If gradients aren't showing:
```html
<!-- Check these classes are present -->
bg-gradient-to-r from-purple-500 to-pink-500
```

2. **Responsive Issues**
If elements look wrong on mobile:
- Verify `md:` and `lg:` prefixes are present
- Check the viewport meta tag is present in `<head>`

3. **Missing Styles**
If Tailwind styles aren't working:
- Confirm the Tailwind CDN is properly linked:
```html
<script src="https://cdn.tailwindcss.com"></script>
```

### Need Help?
- Double-check all changes against the original code
- Use browser developer tools (F12) to inspect elements
- Ensure all HTML tags are properly closed
- Verify file paths for links are correct relative to your project structure

Remember to always test your changes across different devices and browsers to ensure consistency.