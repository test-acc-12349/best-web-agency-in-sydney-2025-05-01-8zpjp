# Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing your web agency landing page. Follow these step-by-step instructions to make common updates while preserving the design integrity.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your brand name and navigation menu. To update:

1. **Company Name:**
```html
<a href="#" class="text-2xl font-bold bg-gradient-to-r from-blue-500 to-purple-600 bg-clip-text text-transparent">WebAgency</a>
```
- Replace "WebAgency" with your company name
- Keep the surrounding classes to maintain the gradient effect

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="hover:text-blue-400 transition-colors duration-300">Features</a>
    <!-- Additional menu items -->
</div>
```
- Update text between `<a>` tags
- Maintain the `hover:text-blue-400` class for consistent hover effects

### Hero Section
Located at the top of the page:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold mb-6 bg-gradient-to-r from-blue-400 to-purple-500 bg-clip-text text-transparent">Best Web Agency In Sydney</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">Grow your business with clicks</p>
```
- Update heading and subheading text
- Keep responsive text classes (`text-4xl md:text-5xl lg:text-6xl`)
- Maintain gradient effect classes

### Features Section
To modify feature cards:

```html
<div class="bg-gray-900 rounded-2xl p-8 hover:transform hover:scale-105 transition-all duration-300">
    <div class="w-16 h-16 bg-blue-600 rounded-full flex items-center justify-center mb-6">
        <i class="fas fa-laptop-code text-2xl"></i>
    </div>
    <h3 class="text-xl font-bold mb-4">Easy to Use</h3>
    <p class="text-gray-400">Intuitive interface designed for seamless user experience...</p>
</div>
```
- Update icon: Change `fa-laptop-code` to any [Font Awesome](https://fontawesome.com/icons) icon
- Modify heading and description text
- Maintain hover effect classes for consistency

## Managing Links

### Navigation Links
Current internal links point to page sections:

```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update:
1. Ensure section IDs match link targets
2. For external links, replace "#" with full URL:
```html
<a href="https://your-site.com/page">Link Text</a>
```

### Call-to-Action Buttons
Current CTA links:
```html
<a href="https://fixrr.online" class="px-8 py-4 bg-blue-600 hover:bg-blue-700 rounded-full">Get Started Now</a>
```

To update:
1. Replace `https://fixrr.online` with your target URL
2. Maintain button classes for consistent styling
3. Test links after updating

## Adding Privacy and Terms Pages

### Footer Link Setup
Locate the legal section in the footer:

```html
<div>
    <h3 class="text-xl font-bold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link privacy and terms pages:

1. Create new HTML files:
   - `privacy.html`
   - `terms.html`

2. Update footer links:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Terms of Service</a></li>
```

3. For subdirectory placement:
```html
<li><a href="./legal/privacy.html">Privacy Policy</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Gradient Text**
If gradient text disappears:
```html
<!-- Ensure these classes are present -->
bg-gradient-to-r from-blue-400 to-purple-500 bg-clip-text text-transparent
```

2. **Responsive Issues**
Check responsive classes:
- `md:` prefix for tablet (768px+)
- `lg:` prefix for desktop (1024px+)
- Example: `text-4xl md:text-5xl lg:text-6xl`

3. **Missing Icons**
Verify Font Awesome inclusion:
```html
<link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
```

### Need Help?
- Check Tailwind CSS documentation for class references
- Verify all section IDs match navigation links
- Test responsive design using browser dev tools
- Ensure all external links include `https://`

Remember to test all changes across different devices and browsers before deploying to production.