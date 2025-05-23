# Texas Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web Design landing page. It's written for beginners with no prior coding experience.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Policy Pages](#adding-policy-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Main Sections
The landing page is divided into these key sections:

1. Header (Navigation)
2. Hero Section
3. Features
4. Benefits
5. Video
6. FAQ
7. Call to Action
8. Footer

### How to Update Text Content

#### Header Text
Find the navigation section:
```html
<nav class="container mx-auto px-6 py-4">
    <a href="/" class="text-2xl font-bold text-white">TWD</a>
```
To change the logo text, replace "TWD" with your desired text.

#### Hero Section Text
Locate the hero section:
```html
<h1 class="text-4xl md:text-6xl font-bold mb-6 leading-tight">Texas Web Design</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">Best Websites In Texas</p>
```
Simply replace the text between the tags while keeping the tags intact.

### Understanding Tailwind Classes

Key classes used in this template:

- Text Sizes:
  - `text-xl`: Medium text
  - `text-2xl`: Larger text
  - `text-4xl`: Very large text
  - Add `md:` prefix for responsive sizing (e.g., `md:text-6xl`)

- Colors:
  - `text-gray-100`: Light gray text
  - `text-blue-400`: Blue accent color
  - `bg-gray-900`: Dark background
  - `hover:text-blue-400`: Blue text on hover

Example of updating colors:
```html
<!-- Original -->
<div class="bg-gray-900 text-gray-100">

<!-- Changed to blue theme -->
<div class="bg-blue-900 text-gray-100">
```

## Managing Links

### Current Link Structure

1. Navigation Menu Links:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#video">Watch</a>
    <a href="#faq">FAQ</a>
</div>
```

2. Call-to-Action Links:
```html
<a href="https://twd.com" class="inline-block px-8 py-4 bg-blue-600">
```

### Updating Links

1. Internal Links (Same Page):
   - Keep the `#` symbol
   - Match the ID of the section you're linking to
   ```html
   <!-- Example: Linking to Features section -->
   <a href="#features">Features</a>
   ```

2. External Links:
   - Replace `https://twd.com` with your actual website URL
   ```html
   <!-- Example -->
   <a href="https://your-actual-website.com">
   ```

## Adding Policy Pages

### Footer Policy Links
Locate the footer links section:
```html
<ul class="space-y-2 text-gray-400">
    <li><a href="#" class="hover:text-blue-400 transition duration-300">Privacy Policy</a></li>
    <li><a href="#" class="hover:text-blue-400 transition duration-300">Terms of Service</a></li>
</ul>
```

To link to policy pages:

1. Create your policy pages (privacy.html, terms.html)
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-blue-400 transition duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-blue-400 transition duration-300">Terms of Service</a></li>
```

## Troubleshooting

Common Issues and Solutions:

1. Links Not Working
   - Check for typos in href attributes
   - Verify file names match exactly
   - Ensure files are in the correct directory

2. Styling Issues
   - Maintain the same class structure as original elements
   - Don't remove responsive classes (those starting with `md:`)
   - Keep the `transition duration-300` classes for smooth hover effects

3. Mobile Menu Not Showing
   - Don't remove the `hidden md:flex` classes from navigation
   - Keep the mobile menu button intact:
   ```html
   <button class="md:hidden text-white">
       <i class="fas fa-bars text-2xl"></i>
   </button>
   ```

Remember:
- Always make a backup before editing
- Test changes on both desktop and mobile views
- Maintain the existing class structure for consistent styling
- Keep the Font Awesome and Tailwind CDN links in the header

Need help? Contact the development team at admin@twd.com