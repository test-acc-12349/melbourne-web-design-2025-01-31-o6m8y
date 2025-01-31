# Melbourne Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Melbourne Web Design landing page. It's written for beginners and provides step-by-step instructions for common updates.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your logo and navigation menu. To update:

1. Change the logo text:
```html
<!-- Find this line in the header -->
<a href="/" class="text-2xl font-bold text-blue-600">MWD</a>
```
Replace "MWD" with your desired text.

### Hero Section
Located at the top of the page, containing main headings:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">Melbourne Web Design</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">Best Websites In Melbourne</p>
```

The text sizes are controlled by these Tailwind classes:
- `text-4xl`: Large on mobile
- `md:text-5xl`: Larger on medium screens
- `lg:text-6xl`: Largest on large screens

### Features Section
To modify feature cards:

1. Locate the feature cards in the `features` section:
```html
<div class="p-8 bg-white rounded-2xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mb-6">
        <i class="fas fa-paint-brush text-2xl text-blue-600"></i>
    </div>
    <h3 class="text-xl font-bold mb-4">Custom Design</h3>
    <p class="text-gray-600">Unique, tailored designs...</p>
</div>
```

2. To change icons:
   - Replace `fa-paint-brush` with any [Font Awesome icon name](https://fontawesome.com/icons)
   - Keep the `fas` prefix

### Common Tailwind Classes Explained
- `container mx-auto`: Centers content and sets max-width
- `px-6`: Adds horizontal padding
- `py-4`: Adds vertical padding
- `text-gray-600`: Sets text color
- `hover:text-blue-600`: Changes text color on hover
- `transition-colors`: Enables smooth color transitions

## Managing Links

### Navigation Menu Links
Current navigation links are:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update:
1. Internal links (same page sections):
   - Keep the `#` prefix
   - Match the `id` of the target section
   - Example: `href="#features"` jumps to `<section id="features">`

2. External links:
   - Replace `href="https://mwd.com"` with your actual URL
   - Example: `href="https://yourwebsite.com"`

### Call-to-Action Buttons
Located in hero and CTA sections:

```html
<a href="https://mwd.com" class="inline-block px-8 py-4 bg-blue-600 text-white rounded-full">Start Your Project</a>
```

Replace `https://mwd.com` with your desired destination URL.

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your website directory:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Locate these lines in the footer:

```html
<ul class="space-y-2 text-gray-400">
    <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

Replace with:

```html
<ul class="space-y-2 text-gray-400">
    <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Check that section `id` attributes match link `href` values
   - Example: `href="#features"` needs `<section id="features">`

2. **Icons Not Showing**
   - Verify Font Awesome CSS is loaded
   - Check icon class names against [Font Awesome documentation](https://fontawesome.com/icons)

3. **Responsive Design Issues**
   - Keep Tailwind's responsive prefixes (`md:`, `lg:`)
   - Test on different screen sizes
   - Don't remove `container` classes

### Need Help?
- Double-check all changes against the original code
- Use browser developer tools (F12) to inspect elements
- Maintain consistent spacing and indentation
- Keep backup copies of working code

Remember to test all changes across different devices and browsers before publishing to your live site.