# Roofing Pro Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Roofing Pro landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Company Name and Logo
The company name appears in two locations:
```html
<!-- Header -->
<h1 class="text-2xl font-bold text-blue-600">Roofing Pro</h1>

<!-- Footer -->
<h4 class="text-xl font-bold mb-4">Roofing Pro</h4>
```
To update:
1. Replace "Roofing Pro" with your company name
2. Adjust text size using Tailwind classes if needed:
   - `text-2xl` = larger size
   - `text-xl` = smaller size

### Hero Section Text
Located near the top of the page:
```html
<h2 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">
    Trusted Roofing and Siding Contractor
</h2>
<p class="text-xl text-gray-600 mb-8">
    Professional roofing and siding solutions for your home
</p>
```
To modify:
1. Replace the heading and paragraph text
2. Maintain responsive sizing classes:
   - `text-4xl` (mobile)
   - `md:text-5xl` (tablet)
   - `lg:text-6xl` (desktop)

### Service Cards
Each service card follows this structure:
```html
<div class="bg-white rounded-xl shadow-lg p-8 hover:shadow-xl transition duration-300">
    <i class="fas fa-home text-4xl text-blue-600 mb-4"></i>
    <h4 class="text-xl font-semibold mb-4">Roofing Services</h4>
    <p class="text-gray-600">Professional roofing installation, repair, and maintenance services.</p>
</div>
```
To update:
1. Change the icon by modifying the `fa-home` class to another [Font Awesome icon](https://fontawesome.com/icons)
2. Update heading and description text
3. Maintain spacing classes (`mb-4`, `p-8`) for consistent layout

## Fixing Broken Links

### Navigation Menu Links
Current navigation structure:
```html
<div class="hidden md:flex space-x-8">
    <a href="#services" class="text-gray-600 hover:text-blue-600 transition duration-300">Services</a>
    <a href="#estimates" class="text-gray-600 hover:text-blue-600 transition duration-300">Estimates</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600 transition duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-blue-600 transition duration-300">Contact</a>
</div>
```
To update:
1. Internal links (starting with #) connect to section IDs on the same page
2. For external pages, replace with full URLs:
   ```html
   <a href="https://example.com/services" class="text-gray-600 hover:text-blue-600 transition duration-300">
   ```

### Contact Information
Update email address in two locations:
```html
<!-- Contact Section -->
<a href="mailto:john@lana.com" class="text-blue-600 text-xl font-semibold">

<!-- Footer -->
<p class="text-gray-400">Email: john@lana.com</p>
```

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the Quick Links section:
```html
<div>
    <h4 class="text-xl font-bold mb-4">Quick Links</h4>
    <ul class="space-y-2">
        <!-- Existing links -->
        <li><a href="privacy.html" class="text-gray-400 hover:text-white transition duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="text-gray-400 hover:text-white transition duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Creating Policy Pages
1. Create new files:
   - `privacy.html`
   - `terms.html`
2. Use consistent styling:
   ```html
   <link rel="stylesheet" href="https://cdn.tailwindcss.com">
   <div class="container mx-auto px-4 py-12">
       <h1 class="text-3xl font-bold mb-6">Privacy Policy</h1>
       <!-- Content here -->
   </div>
   ```

## Troubleshooting

### Common Issues

1. **Broken Responsive Design**
   - Check for missing responsive classes (`md:`, `lg:` prefixes)
   - Verify container class is present: `container mx-auto`

2. **Missing Icons**
   - Ensure Font Awesome CSS is loaded
   - Check icon class names against [Font Awesome documentation](https://fontawesome.com)

3. **Navigation Links Not Working**
   - Verify section IDs match href attributes
   - Check for typos in URLs
   - Test all links in different browsers

### Need Help?
If you encounter issues:
1. Inspect the page using browser developer tools (F12)
2. Check the console for error messages
3. Verify all required CSS and JavaScript files are loading
4. Test on multiple devices and browsers

Remember to backup your files before making significant changes, and always test updates in a development environment first.