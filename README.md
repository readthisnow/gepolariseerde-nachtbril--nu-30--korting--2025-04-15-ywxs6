# NachtBril Landing Page - Maintenance Guide

This guide will help you maintain and customize the NachtBril landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text:**
```html
<!-- Find this line in the header -->
<a href="/" class="text-2xl font-bold text-blue-600">NachtBril</a>
```
Simply replace "NachtBril" with your desired text.

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Kenmerken</a>
    <!-- Additional menu items -->
</div>
```
Replace "Kenmerken" and other menu text while keeping the classes intact.

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">
    Gepolariseerde NachtBril
    <span class="block text-blue-600 mt-2">Nu 30% Korting!</span>
</h1>
```
- Update the main heading and discount text
- Keep the responsive classes (`text-4xl md:text-5xl lg:text-6xl`) to maintain proper sizing across devices

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white p-8 rounded-2xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="text-blue-600 text-4xl mb-4">🌙</div>
    <h3 class="text-xl font-bold mb-4">Premium Nachtzicht</h3>
    <p class="text-gray-600">Revolutionaire technologie voor kristalhelder zicht in het donker!</p>
</div>
```
- Change emoji by replacing the character
- Update heading and description text
- Maintain the class structure for consistent styling

## Managing Links

### Navigation Links
Current navigation links are:
```html
<a href="#features">Kenmerken</a>
<a href="#benefits">Voordelen</a>
<a href="#faq">FAQ</a>
<a href="https://nachtbril.com/shop">Koop Nu</a>
```

To update:
1. Internal links (starting with #) point to section IDs on the page
2. External links (starting with http) point to other websites
3. Replace `href` values with your desired destinations

Example updating shop link:
```html
<!-- Original -->
<a href="https://nachtbril.com/shop">Koop Nu</a>

<!-- Updated -->
<a href="https://yournewshop.com">Koop Nu</a>
```

### Call-to-Action Buttons
Located throughout the page:
```html
<a href="https://nachtbril.com/shop" class="inline-block bg-blue-600 text-white text-lg px-8 py-4 rounded-full hover:bg-blue-700 transition-all duration-300 transform hover:scale-105 shadow-lg">
    DIRECT BESTELLEN - 30% KORTING
</a>
```
Update all instances of the shop URL to maintain consistency.

## Adding Privacy and Terms Pages

### Footer Links
Current placeholder links:
```html
<ul class="space-y-2">
    <li><a href="#" class="hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="hover:text-blue-400 transition-colors duration-300">Algemene Voorwaarden</a></li>
</ul>
```

To link to new pages:
1. Create `privacy.html` and `terms.html` in your root directory
2. Update the links:
```html
<li><a href="privacy.html" class="hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-blue-400 transition-colors duration-300">Algemene Voorwaarden</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Layout:**
   - Check that you haven't removed any essential Tailwind CSS classes
   - Verify all `div` tags are properly closed
   - Maintain the responsive classes (md:, lg:) for proper mobile display

2. **Links Not Working:**
   - Ensure file names match exactly (case-sensitive)
   - Check that files are in the correct directory
   - Verify all `href` attributes start with either `#`, `./`, or `https://`

3. **Styling Issues:**
   - Don't remove classes containing `transition`, `duration`, or `hover:`
   - Maintain the hierarchy of container > row > column elements
   - Keep the `container mx-auto px-4` classes on main sections

### Need Help?
If you encounter issues:
1. Check the HTML structure matches the original
2. Verify all required CSS classes are present
3. Test the page on different devices
4. Ensure all links point to valid destinations

Remember: Always backup your files before making changes!

This guide specifically references the NachtBril landing page structure. For additional customization needs, consult the Tailwind CSS documentation or seek professional assistance.