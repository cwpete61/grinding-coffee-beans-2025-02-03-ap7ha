# CoffeeMax Landing Page Maintenance Guide

This guide will help you maintain and customize the CoffeeMax landing page. It's written for beginners with no prior coding experience.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. Change company name:
```html
<!-- Find this line in the header section -->
<a href="/" class="text-2xl font-bold text-gray-900">CoffeeMax</a>
```
Simply replace "CoffeeMax" with your desired name.

### Hero Section
Located at the top of the page with the main headline:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold tracking-tight text-gray-900 mb-8">
    Grinding Coffee Beans
</h1>
<p class="text-xl md:text-2xl font-medium text-gray-600 mb-12">
    Create Great Coffee at Home
</p>
```

The text sizes are controlled by these Tailwind classes:
- `text-4xl`: Large on mobile
- `md:text-5xl`: Larger on medium screens
- `lg:text-6xl`: Largest on large screens

### Features Section
To modify feature cards:

1. Locate the feature cards in the grid:
```html
<div class="bg-white p-8 rounded-xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="text-blue-600 mb-4">
        <i class='bx bx-check-circle text-4xl'></i>
    </div>
    <h3 class="text-xl font-bold mb-4">Easy Process</h3>
    <p class="text-gray-600">Simple steps to achieve the perfect grind every time.</p>
</div>
```

2. Update the icon by changing the `bx-check-circle` class to any other [Boxicons](https://boxicons.com/) class
3. Modify the heading and paragraph text as needed

## Managing Links

### Navigation Menu Links
The main navigation links are in the header:

```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">FAQ</a>
    <a href="https://coffeemax.com" class="inline-flex items-center...">Get Started</a>
</div>
```

To update:
1. Internal links (starting with #) connect to page sections
2. Change `href="https://coffeemax.com"` to your actual website URL

### Call-to-Action (CTA) Links
Located in multiple sections:

```html
<!-- Hero Section CTA -->
<a href="https://coffeemax.com" class="inline-flex items-center...">Start Brewing Today</a>

<!-- Bottom CTA Section -->
<a href="https://coffeemax.com" class="inline-flex items-center...">Get Started Now</a>
```

Update all instances of `https://coffeemax.com` to your desired URL.

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
1. Create two new files in your website folder:
   - `privacy.html`
   - `terms.html`

### Step 2: Update Footer Links
Locate this section in the footer:

```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

Replace the `#` placeholders:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Links**
   - Check that all `href` attributes have correct URLs
   - Internal links should start with `#` (e.g., `#features`)
   - External links should include `https://`

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - Keep the `container` class on parent elements
   - Maintain the existing grid structure using `grid-cols-*` classes

3. **Icon Problems**
   - Ensure the Boxicons CSS file is properly linked in the header
   - Check that icon class names match exactly with Boxicons documentation
   - Maintain the `bx` prefix for all icons

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Verify links using your browser's developer tools (F12)
- Test the page on different screen sizes using browser developer tools

Remember to always backup your code before making changes, and test thoroughly after each modification.