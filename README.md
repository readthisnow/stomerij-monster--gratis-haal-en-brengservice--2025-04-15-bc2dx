# Stomerij Monster Landing Page - Maintenance Guide

This guide will help you maintain and customize the Stomerij Monster landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To update:

1. **Company Name/Logo**
```html
<!-- Find this line in the header -->
<a href="/" class="text-2xl font-bold text-blue-600">Stomerij Monster</a>
```
Simply replace "Stomerij Monster" with your desired text.

2. **Navigation Menu Items**
```html
<div class="hidden md:flex space-x-8">
    <a href="#diensten" class="hover:text-blue-600 transition-colors duration-300">Diensten</a>
    <!-- Additional menu items -->
</div>
```
Update the text between `<a>` tags to change menu items.

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">
    Stomerij Monster
    <span class="block text-blue-600 mt-2">Gratis Haal- en Brengservice!</span>
</h1>
```
- To modify the main heading, change "Stomerij Monster"
- For the subheading, update the text within the `<span>` tag
- The classes `text-4xl`, `md:text-5xl`, and `lg:text-6xl` control text size at different screen sizes

### Tailwind CSS Tips for Beginners
- Numbers in classes (like `text-4xl`) indicate size
- `md:` and `lg:` prefixes apply styles at medium and large screens
- Color classes follow the pattern: `text-{color}-{shade}` (e.g., `text-blue-600`)
- Spacing classes use `m` for margin and `p` for padding (e.g., `mb-6` = margin-bottom)

## Managing Links

### Navigation Menu Links
Current internal links:
```html
<a href="#diensten">Diensten</a>
<a href="#voordelen">Voordelen</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
To update:
1. The `#` symbol indicates an internal page section
2. Ensure the href matches the `id` of the target section
3. Example: `href="#diensten"` jumps to `<section id="diensten">`

### Call-to-Action Buttons
```html
<a href="https://wasserettewestland.nl" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-full">
    Direct Reserveren
</a>
```
To update:
1. Replace `https://wasserettewestland.nl` with your desired URL
2. Keep the classes to maintain styling
3. Update button text between the tags

## Adding Privacy and Terms Pages

### Footer Links Setup
Current placeholder links:
```html
<ul class="space-y-2">
    <li><a href="#" class="hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="hover:text-blue-400 transition-colors duration-300">Algemene Voorwaarden</a></li>
</ul>
```

To add proper links:
1. Create new files named `privacy.html` and `terms.html`
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-blue-400 transition-colors duration-300">Algemene Voorwaarden</a></li>
```

### Maintaining Consistent Styling
When creating new pages:
1. Copy the header and footer from `index.html`
2. Use the same Tailwind CSS and Alpine.js includes:
```html
<link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
<script defer src="https://unpkg.com/alpinejs@3.x.x/dist/cdn.min.js"></script>
```

## Troubleshooting

Common Issues:
1. **Broken Internal Links**
   - Ensure section `id` attributes match href values exactly
   - Check for typos in both the link and section ID
   - IDs are case-sensitive

2. **Responsive Design Issues**
   - Test at different screen sizes using browser developer tools
   - Check that `md:` and `lg:` classes are properly applied
   - Maintain the existing responsive class structure

3. **Style Changes Not Appearing**
   - Verify Tailwind CSS is properly loaded
   - Check for typos in class names
   - Classes must be exact matches (e.g., `text-blue-600`, not `text-blue`)

Need additional help? Contact your web developer or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).