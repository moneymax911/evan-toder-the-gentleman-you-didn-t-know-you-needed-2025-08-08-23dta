# Landing Page Maintenance Guide

This guide will help you maintain and customize the Evan Toder landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the navigation menu and logo. To update:

1. **Logo Text (ET)**
```html
<a href="#" class="text-xl font-bold tracking-tight text-white hover:text-indigo-400">ET</a>
```
- Replace "ET" with your desired text
- Adjust size using `text-xl` (options: text-sm, text-base, text-lg, text-2xl)

2. **Navigation Menu Items**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-300 hover:text-white">Features</a>
    <!-- Other menu items -->
</div>
```
- Update text between `<a>` tags
- Maintain the `hidden md:flex` class for mobile responsiveness

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6">
    Evan Toder: The Gentleman You Didn't Know You Needed
</h1>
```
- Update heading text while keeping the classes
- Text sizes are responsive:
  - Mobile: `text-4xl`
  - Tablet: `md:text-5xl`
  - Desktop: `lg:text-6xl`

### Tailwind CSS Class Guide
Common classes used throughout:
- Text colors: `text-white`, `text-gray-300`, `text-gray-400`
- Background colors: `bg-gray-900`, `bg-gray-800`, `bg-gray-700`
- Spacing: 
  - Margin: `m-4`, `mb-6`, `mt-12`
  - Padding: `p-8`, `py-24`, `px-6`
- Hover effects: `hover:text-white`, `hover:bg-gray-700`

## Fixing Broken Links

### Current Link Structure
1. **Internal Navigation Links**
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
To update:
- Ensure section IDs match these href values
- Add new sections by creating a div with matching ID:
```html
<section id="new-section">
    <!-- Content -->
</section>
```

2. **External Links**
```html
<a href="https://pofree.org/" class="inline-block bg-indigo-600">
    Book Your Experience
</a>
```
To update:
- Replace `https://pofree.org/` with your desired URL
- Test links before deploying

3. **Email Links**
```html
<a href="mailto:MaleGigolo@EvanTodersPlace.com">
    MaleGigolo@EvanTodersPlace.com
</a>
```
- Update both the href and display text with your email

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links in the Quick Links section:
```html
<div>
    <h3 class="text-xl font-bold mb-4">Quick Links</h3>
    <ul class="space-y-2">
        <!-- Existing links -->
        <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Creating New Pages
1. Create `privacy.html` and `terms.html` in the same directory
2. Copy the header and footer from `index.html`
3. Add content between them
4. Maintain consistent styling:
```html
<main class="bg-gray-900 text-gray-100 py-24 px-6">
    <div class="container mx-auto max-w-4xl">
        <h1 class="text-3xl md:text-4xl font-bold mb-8">Privacy Policy</h1>
        <!-- Content -->
    </div>
</main>
```

## Troubleshooting

### Common Issues
1. **Broken Responsive Design**
- Check for `md:` and `lg:` prefixes in classes
- Ensure the viewport meta tag is present:
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

2. **Missing Styles**
- Verify Tailwind CSS link is working:
```html
<link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
```

3. **Non-functioning Links**
- Check for typos in href attributes
- Verify section IDs exist and match exactly
- Test all links in different browsers

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Use browser developer tools (F12) to inspect elements
- Test on multiple devices and browsers

Remember to always backup your files before making changes and test thoroughly before deploying to production.