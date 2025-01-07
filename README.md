# Ultimate Website Builder - Landing Page Maintenance Guide

This guide will help you maintain and customize the Ultimate Website Builder landing page. Whether you're new to web development or just getting started, follow these instructions to make updates while preserving the design and functionality.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Fixing and Managing Links](#fixing-and-managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text:**
```html
<!-- Find this section in the header -->
<div class="text-2xl font-bold bg-gradient-to-r from-blue-500 to-purple-600 bg-clip-text text-transparent">
    UWB  <!-- Change this text to your brand name -->
</div>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <!-- Update these link texts as needed -->
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

### Hero Section
To modify the main headline and subheading:

```html
<h1 class="text-4xl md:text-6xl lg:text-7xl font-bold mb-8 bg-gradient-to-r from-blue-400 to-purple-500 bg-clip-text text-transparent">
    Ultimate Website Builder  <!-- Update main headline -->
</h1>
<p class="text-xl md:text-2xl lg:text-3xl text-gray-300 mb-12">
    Get Your Custom Website In 2 Minutes  <!-- Update subheading -->
</p>
```

### Tailwind CSS Tips
- Font sizes use this pattern: `text-sm`, `text-base`, `text-lg`, `text-xl`, etc.
- Colors follow: `text-gray-100`, `bg-blue-500`, etc.
- Spacing uses increments of 4: `p-4` (padding), `m-4` (margin)
- Responsive prefixes: `md:` (medium screens), `lg:` (large screens)

## Fixing and Managing Links

### Navigation Links
Update all navigation href attributes:

```html
<!-- Current navigation links -->
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>

<!-- "Get Started" button -->
<a href="https//:uwb.com" class="bg-blue-600 hover:bg-blue-700...">
    Get Started
</a>
```

To update links:
1. Replace `#features` with your section ID or full URL
2. Fix the "Get Started" link by updating `https//:uwb.com` to your actual URL
3. Ensure all URLs start with `https://`

### Social Media Links
Located in the footer:

```html
<div class="flex space-x-4">
    <!-- Update href attributes with your social media profiles -->
    <a href="#" class="text-gray-400 hover:text-blue-400">
        <i class="fab fa-twitter text-xl"></i>
    </a>
    <a href="#" class="text-gray-400 hover:text-blue-400">
        <i class="fab fa-facebook text-xl"></i>
    </a>
    <a href="#" class="text-gray-400 hover:text-blue-400">
        <i class="fab fa-instagram text-xl"></i>
    </a>
</div>
```

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your project directory:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Replace the placeholder links in the footer:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <!-- Update these href attributes -->
        <li><a href="privacy.html" class="hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="hover:text-blue-400 transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Step 3: Maintain Consistent Styling
Copy these classes to maintain consistent link styling:
```html
class="hover:text-blue-400 transition-colors duration-300"
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Links**
   - Check for typos in URLs
   - Ensure all URLs start with `https://`
   - Verify file paths for internal links

2. **Responsive Design Issues**
   - Keep the `md:` and `lg:` prefixes in Tailwind classes
   - Don't remove the `container` class from section wrappers
   - Maintain the existing grid structure in features and benefits sections

3. **Style Problems**
   - Don't remove the `bg-gray-900` class from the body
   - Keep gradient classes intact for maintaining design
   - Preserve the `transition-all duration-300` classes for animations

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Test responsive design using browser developer tools

Remember to always make a backup of your files before making significant changes!