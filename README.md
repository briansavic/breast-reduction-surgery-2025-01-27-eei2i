# Landing Page Maintenance Guide
## The Karri Clinic Website

This guide provides detailed instructions for maintaining and customizing the breast reduction surgery landing page.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the clinic name and navigation menu:
```html
<div class="text-xl font-semibold text-gray-700">
    The Karri Clinic  <!-- Change clinic name here -->
</div>
```
To modify:
1. Locate this section at the top of the page
2. Replace "The Karri Clinic" with your desired text
3. Adjust text size by changing `text-xl` to `text-lg` (smaller) or `text-2xl` (larger)

### Hero Section
The main headline and introduction:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-8 leading-tight">
    Breast Reduction Surgery  <!-- Update main headline here -->
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12 leading-relaxed">
    Experience relief...  <!-- Update introduction text here -->
</p>
```
Tailwind CSS explanation:
- `text-4xl`: Base text size
- `md:text-5xl`: Text size on medium screens
- `lg:text-6xl`: Text size on large screens
- `mb-8`: Margin bottom spacing

### Features Section
To add or modify features:
1. Locate the `grid grid-cols-1 md:grid-cols-3 gap-12` div
2. Each feature is structured as:
```html
<div class="bg-white p-8 rounded-xl shadow-lg hover:shadow-xl transition duration-300">
    <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mb-6">
        <i class="fas fa-heart text-blue-600 text-2xl"></i>  <!-- Change icon here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Reduced Discomfort</h3>  <!-- Change title -->
    <p class="text-gray-600 leading-relaxed">Experience significant relief...</p>  <!-- Change description -->
</div>
```

## Fixing Broken Links

### Navigation Menu Links
Current internal links:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600 transition duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600 transition duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-blue-600 transition duration-300">Contact</a>
</div>
```
To update:
1. For internal links (same page sections), keep the `#` prefix
2. For external links, replace with full URL: `href="https://example.com"`
3. Verify each section ID matches its link (e.g., `#features` should match `id="features"`)

### Consultation Button
Update the consultation link:
```html
<a href="https://thekarriclinic.co.uk/" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-lg">
```
Replace `https://thekarriclinic.co.uk/` with your booking page URL

## Linking Privacy and Terms Pages

### Footer Links
Current placeholder links:
```html
<div class="space-y-4">
    <h3 class="text-xl font-semibold text-white mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create privacy.html and terms.html in your website directory
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition duration-300">Terms of Service</a></li>
```

## Troubleshooting

Common Issues:
1. **Broken Internal Links**
   - Check that section IDs match exactly with href values
   - IDs are case-sensitive
   - Example: `href="#FAQ"` won't link to `id="faq"`

2. **Responsive Design Issues**
   - If text appears too large/small, adjust the responsive classes:
   - Format: `text-base md:text-lg lg:text-xl`
   - Sizes increase from left to right

3. **Icon Not Showing**
   - Verify Font Awesome is properly loaded
   - Check icon class names against [Font Awesome documentation](https://fontawesome.com/icons)
   - Example: `<i class="fas fa-heart"></i>`

Remember to:
- Test all links after making changes
- View the page at different screen sizes
- Keep backup copies of working versions
- Validate HTML using [W3C Validator](https://validator.w3.org/)

Need additional help? Contact your web development team or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).