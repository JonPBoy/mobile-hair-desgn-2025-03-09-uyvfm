# Mobile Hair Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Mobile Hair Design landing page. It's written for beginners and provides detailed instructions for common updates and modifications.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and brand name. To update:

1. **Company Name:**
```html
<h1 class="text-2xl font-['Playfair_Display'] font-bold text-gray-800">Mobile Hair Design</h1>
```
- Replace "Mobile Hair Design" with your desired company name
- The `text-2xl` class controls size (options: text-sm, text-base, text-lg, text-2xl, text-3xl)

2. **Navigation Menu Items:**
```html
<a href="#services" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Services</a>
```
- Update text between `<a>` tags
- The `text-gray-600` class controls text color
- `hover:text-gray-900` changes color on mouse hover

### Hero Section
Located at the top of the page:
```html
<h2 class="text-4xl md:text-5xl lg:text-6xl font-['Playfair_Display'] font-bold text-gray-900 mb-6">Professional Hair Styling at Your Doorstep</h2>
```
- Update headline text between the `<h2>` tags
- Size classes explain the responsive behavior:
  - `text-4xl`: mobile screens
  - `md:text-5xl`: medium screens
  - `lg:text-6xl`: large screens

### Services Section
To add or modify service cards:
```html
<div class="bg-white p-8 rounded-2xl shadow-lg hover:shadow-xl transition-all duration-300 transform hover:-translate-y-1">
    <div class="w-16 h-16 bg-rose-100 rounded-full flex items-center justify-center mb-6">
        <!-- Icon SVG here -->
    </div>
    <h4 class="text-xl font-semibold mb-4">Expert Hair Extensions</h4>
    <p class="text-gray-600">Professional installation and maintenance of premium hair extensions.</p>
</div>
```
- Copy this entire block to add new services
- Update the heading (`<h4>`) and description (`<p>`) text
- Maintain the class structure for consistent styling

## Managing Links

### Navigation Menu Links
Current internal links:
```html
<a href="#services">Services</a>
<a href="#benefits">Benefits</a>
<a href="#contact">Book Now</a>
```
To update:
1. The `#` symbol indicates an internal page section
2. Ensure the href matches the `id` of the target section
3. For external links, replace with full URL: `href="https://example.com"`

### Phone Number Links
Located in multiple places:
```html
<a href="tel=9493072748">Call Now</a>
```
To update:
1. Replace `9493072748` with new phone number
2. Keep the `tel=` prefix
3. Remove any spaces or special characters

### Email Links
Located in the footer:
```html
<p class="text-gray-600">Email: jonpboy@gmail.com</p>
```
To make clickable:
```html
<p class="text-gray-600">Email: <a href="mailto:jonpboy@gmail.com">jonpboy@gmail.com</a></p>
```

## Adding Privacy and Terms Pages

### Footer Modification
Add these links to the footer section:
```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
    <!-- Existing content -->
    <div>
        <h4 class="text-lg font-semibold mb-4">Legal</h4>
        <ul class="space-y-2">
            <li><a href="privacy.html" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Privacy Policy</a></li>
            <li><a href="terms.html" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Terms of Service</a></li>
        </ul>
    </div>
</div>
```

### Creating Policy Pages
1. Create new files named `privacy.html` and `terms.html`
2. Use the same header and footer as `index.html`
3. Maintain consistent styling using the same Tailwind classes

## Troubleshooting

### Common Issues:

1. **Broken Internal Links**
- Verify that section `id` attributes match the href values
- Example: `href="#services"` needs matching `id="services"`

2. **Responsive Design Issues**
- Check responsive class prefixes:
  - `md:` for medium screens
  - `lg:` for large screens
- Test on different devices using browser dev tools

3. **Styling Inconsistencies**
- Keep font families consistent:
  - Headers: `font-['Playfair_Display']`
  - Body text: `font-['Poppins']`
- Maintain color scheme using existing classes:
  - Primary: `bg-rose-500`
  - Text: `text-gray-600`, `text-gray-900`

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Use browser inspector tools to examine element styling
- Test all changes across different screen sizes

Remember to always backup your files before making significant changes.