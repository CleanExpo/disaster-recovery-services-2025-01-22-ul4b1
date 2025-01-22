# Landing Page Maintenance Guide

This guide will help you maintain and customize the Disaster Recovery Services landing page. It's designed for beginners with no prior coding experience.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains your company logo and navigation menu:
```html
<div class="text-2xl font-bold text-blue-600">DRQ</div>
```
- To change the logo text: Replace "DRQ" with your company name
- To modify logo color: Change `text-blue-600` to another color (e.g., `text-red-600`)
- Available color options: red, blue, green, yellow, purple (with shades 100-900)

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">
    Disaster Recovery Services
</h1>
```
- To change heading size:
  - `text-4xl`: Mobile size
  - `md:text-5xl`: Tablet size
  - `lg:text-6xl`: Desktop size
- Adjust spacing with `mb-6` (margin-bottom)

### Services Cards
Each service card follows this structure:
```html
<div class="bg-white rounded-xl shadow-lg p-8 hover:shadow-xl transition-shadow duration-300">
    <i class="fas fa-water text-4xl text-blue-600 mb-4"></i>
    <h3 class="text-xl font-bold mb-4">Water Damage Restoration</h3>
    <p class="text-gray-600">Professional water damage restoration services...</p>
</div>
```
- To add a new service: Copy entire `<div>` block
- Change icon: Replace `fa-water` with another [Font Awesome icon](https://fontawesome.com/icons)
- Modify text: Update the `<h3>` and `<p>` content

## Fixing Broken Links

### Navigation Menu Links
Current navigation links:
```html
<div class="hidden md:flex space-x-8">
    <a href="#services" class="text-gray-700 hover:text-blue-600">Services</a>
    <a href="#benefits" class="text-gray-700 hover:text-blue-600">Benefits</a>
    <a href="#faq" class="text-gray-700 hover:text-blue-600">FAQ</a>
    <a href="#contact" class="text-gray-700 hover:text-blue-600">Contact</a>
</div>
```
To update:
1. Internal links (same page): Use `#section-id`
2. External links: Use full URL (e.g., `https://example.com`)
3. Email links: Use `mailto:email@example.com`

### Social Media Links
Located in footer:
```html
<div class="flex space-x-4">
    <a href="#" class="hover:text-white transition-colors duration-300">
        <i class="fab fa-facebook"></i>
    </a>
</div>
```
Replace `#` with your social media profile URLs.

## Adding Privacy and Terms Pages

### Step 1: Add Footer Links
Add these lines to the Quick Links section in the footer:
```html
<ul class="space-y-2">
    <!-- Existing links -->
    <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

### Step 2: Create New Pages
1. Create `privacy.html` and `terms.html` in your root directory
2. Copy the header and footer from `index.html`
3. Add your policy content between them

## Troubleshooting

### Common Issues

1. **Broken Layout**
   - Check for missing closing tags (`</div>`)
   - Verify Tailwind CSS classes are spelled correctly
   - Ensure proper nesting of elements

2. **Missing Icons**
   - Verify Font Awesome CSS is loaded
   - Check icon class names against Font Awesome documentation

3. **Non-working Links**
   - Confirm file paths are correct
   - Check for typos in URLs
   - Verify section IDs match href attributes

### CSS Class Reference

Important Tailwind classes used:
- `container`: Centers content and sets max-width
- `mx-auto`: Centers element horizontally
- `px-6`: Adds horizontal padding
- `py-24`: Adds vertical padding
- `grid`: Creates grid layout
- `md:`: Applies styles at medium screen sizes
- `lg:`: Applies styles at large screen sizes

Remember to test all changes across different screen sizes (mobile, tablet, desktop) to ensure responsive design remains intact.

For additional help, consult the [Tailwind CSS documentation](https://tailwindcss.com/docs) or reach out to your development team.