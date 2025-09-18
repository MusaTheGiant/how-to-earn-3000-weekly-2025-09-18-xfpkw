# TXC Mining Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the TXC Mining landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Legal Pages](#adding-legal-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the logo and navigation menu. To modify:

```html
<!-- Logo Text -->
<div class="text-2xl font-bold text-blue-600">TXC Mining</div>
```
- To change the logo text, replace "TXC Mining"
- To adjust logo size, modify `text-2xl` to `text-xl` (smaller) or `text-3xl` (larger)

### Hero Section
Located at the top of the page:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">
    How To Earn $3000 Weekly
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-10">
    Let's Mine TXC Together
</p>
```
- Update headline by changing text within `<h1>` tags
- Modify subheading within the `<p>` tags
- The `md:` and `lg:` prefixes control responsive sizing

### Feature Cards
Each feature card follows this structure:

```html
<div class="p-8 rounded-2xl bg-white shadow-lg hover:shadow-xl transition-all duration-300">
    <h3 class="text-xl font-semibold mb-4">Mine-for-Life</h3>
    <p class="text-gray-600">Secure your future with our lifetime mining opportunity...</p>
</div>
```
To modify:
1. Change card title within `<h3>` tags
2. Update description within `<p>` tags
3. Adjust spacing with `p-8` (padding) or `mb-4` (margin-bottom)

## Managing Links

### Navigation Menu Links
Current navigation structure:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Benefits</a>
    <a href="#contact" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Contact</a>
</div>
```

To update links:
1. Locate the `href` attribute
2. For internal sections, use `#section-id`
3. For external links, use full URL: `https://example.com`

### Call-to-Action Buttons
The main CTA buttons use this format:

```html
<a href="https://minetxc.com/sign-up?sponsor=mtglegacy" class="inline-block px-8 py-4 bg-blue-600 text-white text-lg rounded-full hover:bg-blue-700 transition-all duration-300">
    Start Mining Now
</a>
```

To modify:
1. Update `href` with new destination URL
2. Change button text between `<a>` tags
3. Adjust styling using Tailwind classes:
   - `px-8`: horizontal padding
   - `py-4`: vertical padding
   - `bg-blue-600`: background color
   - `rounded-full`: border radius

## Adding Legal Pages

### Footer Legal Links
Current placeholder structure:

```html
<div>
    <h3 class="text-xl font-bold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add legal pages:
1. Create `privacy.html` and `terms.html` in your root directory
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match href attributes
   - Check for typos in IDs
   - IDs should not contain spaces

2. **Responsive Design Issues**
   - Check mobile view using browser dev tools
   - Verify `md:` and `lg:` prefixes are correct
   - Test different screen sizes

3. **Style Changes Not Applying**
   - Confirm Tailwind CDN is loading
   - Check class name spelling
   - Verify class order (Tailwind uses last-applied rule)

### Need Help?
- Double-check the Tailwind CSS documentation
- Use browser inspector to identify elements
- Test changes in small increments
- Back up your code before making major changes

Remember: Always test your changes across different devices and browsers to ensure consistency.