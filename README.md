# Albert Park Landing Page Maintenance Guide

This guide will help you maintain and customize the Albert Park Accounting Services landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name:**
```html
<a href="#" class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">
    Albert Park <!-- Change this text -->
</a>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a> <!-- Update text here -->
    <a href="#benefits">Benefits</a> <!-- Update text here -->
    <a href="#contact">Contact</a> <!-- Update text here -->
</div>
```

### Hero Section
Located at the top of the page:

```html
<h1 class="text-4xl md:text-6xl lg:text-7xl font-bold mb-8 bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent">
    Albert Park accounting services <!-- Update main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12 max-w-3xl mx-auto">
    Your financial success is our bottom line <!-- Update subheading -->
</p>
```

### Understanding Tailwind Classes
Common classes used in this template:

- Text sizes: `text-sm`, `text-base`, `text-lg`, `text-xl`, `text-2xl`
- Colors: `text-gray-100`, `text-gray-300`, `text-gray-400`
- Spacing: `px-6` (padding left/right), `py-4` (padding top/bottom), `mb-8` (margin bottom)
- Responsive design: `md:text-xl` (applies at medium screens and up)

## Managing Links

### Navigation Menu Links
The page uses internal anchor links. To update:

1. Find the navigation section:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#contact">Contact</a>
</div>
```

2. To link to external pages, replace the `#section-name` with a full URL:
```html
<a href="https://yoursite.com/features">Features</a>
```

### Call-to-Action Buttons
Located in the hero and CTA sections:

```html
<!-- Hero section button -->
<a href="https://theaccountants.com" class="inline-block px-8 py-4 bg-gradient-to-r from-purple-600 to-pink-600 rounded-full">
    Transform Your Finances
</a>

<!-- Update this URL to your actual signup or contact page -->
```

### Footer Links
The footer contains multiple link sections:

```html
<div class="grid grid-cols-1 md:grid-cols-4 gap-12">
    <!-- Services Section -->
    <ul class="space-y-4 text-gray-400">
        <li><a href="#">Tax Optimization</a></li>
        <!-- Add your service page URLs here -->
    </ul>
    
    <!-- Company Section -->
    <ul class="space-y-4 text-gray-400">
        <li><a href="#">About Us</a></li>
        <!-- Add your company page URLs here -->
    </ul>
</div>
```

## Adding Privacy and Terms Pages

### Step 1: Update Footer Links
Locate the Legal section in the footer:

```html
<div>
    <h4 class="text-lg font-semibold mb-6">Legal</h4>
    <ul class="space-y-4 text-gray-400">
        <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Step 2: Create New Pages
1. Create `privacy.html` and `terms.html` in your root directory
2. Copy the header and footer from `index.html` to maintain consistent styling
3. Add your policy content between the header and footer

## Troubleshooting

### Common Issues and Solutions

1. **Broken Links**
   - Check for typos in URLs
   - Ensure files exist in the correct directory
   - Verify that anchor tags (`#section-name`) match section IDs

2. **Responsive Design Issues**
   - Mobile menu not working: Check Alpine.js is properly loaded
   - Layout breaks on mobile: Verify responsive classes (`md:`, `lg:`) are used correctly

3. **Styling Problems**
   - Gradients not showing: Ensure Tailwind CSS is properly loaded
   - Colors not matching: Check for proper color class names in the Tailwind configuration

### Need Help?
If you encounter issues:
1. Check the browser console for errors (F12 key)
2. Verify all CSS and JavaScript files are loading
3. Test the page across different browsers
4. Ensure all external resources (CDN links) are accessible

Remember to always test your changes across different devices and screen sizes before deploying to production.