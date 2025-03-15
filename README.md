# Love Videos Landing Page - Maintenance Guide

This guide will help you maintain and customize the Love Videos landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Text Content Updates

Key sections where you can update text content:

1. **Header/Navigation**
```html
<!-- Located at the top of the page -->
<a href="#" class="text-2xl font-bold">Love Videos</a> <!-- Company name -->
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a> <!-- Navigation menu items -->
    <a href="#benefits">Benefits</a>
    <!-- etc. -->
</div>
```

2. **Hero Section**
```html
<!-- Located in the first section after header -->
<h1 class="text-4xl md:text-6xl font-bold mb-6">Love Videos</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-8">Love</p>
```

3. **Features Section**
```html
<!-- Located in the features grid -->
<div class="p-8 rounded-2xl bg-gray-800">
    <h3 class="text-xl font-bold mb-4">Love</h3>
    <p class="text-gray-400">Experience the power of love through our platform.</p>
</div>
```

### Tailwind CSS Styling

Important classes explained:

1. **Responsive Design Classes**
- `md:text-6xl`: Applies font size on medium screens and larger
- `hidden md:flex`: Hidden on mobile, becomes flex on medium screens
- Example:
```html
<!-- To change mobile/desktop text size -->
<h1 class="text-4xl md:text-6xl"><!-- Change 4xl/6xl to adjust size --></h1>
```

2. **Color Classes**
- `bg-gray-900`: Dark background
- `text-gray-100`: Light text
- `from-pink-500 to-purple-500`: Gradient colors
```html
<!-- To change colors, replace the number (100-900) or color name -->
<div class="bg-gray-900"> <!-- Try bg-slate-900 or bg-gray-800 --></div>
```

## Managing Links

### Navigation Menu Links
Current internal links:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#video">Watch</a>
    <a href="#faq">FAQ</a>
</div>
```
To update:
1. Replace `#section-name` with your new section ID
2. Ensure the corresponding section has matching ID:
```html
<section id="your-new-section">
```

### External Links
Current external links:
```html
<a href="https://love.com" class="px-6 py-2">Get Started</a>
```
To update:
1. Replace `https://love.com` with your desired URL
2. Test the link before deploying

### Social Media Links
Located in footer:
```html
<div class="flex space-x-4">
    <a href="#" class="text-gray-400 hover:text-pink-500">
        <i class="fab fa-twitter"></i>
    </a>
    <!-- Add your social media URLs here -->
</div>
```

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your project:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Replace the placeholder links:
```html
<!-- Original code -->
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-pink-500">Privacy Policy</a></li>
    <li><a href="#" class="text-gray-400 hover:text-pink-500">Terms of Service</a></li>
</ul>

<!-- Updated code -->
<ul class="space-y-2">
    <li><a href="privacy.html" class="text-gray-400 hover:text-pink-500">Privacy Policy</a></li>
    <li><a href="terms.html" class="text-gray-400 hover:text-pink-500">Terms of Service</a></li>
</ul>
```

### Step 3: Maintain Consistent Styling
Copy these classes to maintain consistent link styling:
```html
class="text-gray-400 hover:text-pink-500"
```

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
- Check that section IDs match exactly with href attributes
- IDs are case-sensitive
- Remove any spaces in IDs

2. **Responsive Design Issues**
- Always test on multiple screen sizes
- Use browser dev tools to check breakpoints
- Verify `md:` classes are working correctly

3. **Color Gradient Not Showing**
- Ensure both `from-[color]` and `to-[color]` are present
- Check that `bg-gradient-to-r` is included
- For text gradients, verify `bg-clip-text` and `text-transparent` are present

Remember to:
- Test all changes in multiple browsers
- Validate your HTML
- Back up files before making significant changes
- Keep the responsive design intact by maintaining the `md:` prefixed classes

For additional help or questions, contact the development team at the email provided in the footer.