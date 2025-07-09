# Luxury Bath DG Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Luxury Bath DG landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Navigation Links](#managing-navigation-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. Company Name:
```html
<!-- Located in header section -->
<div class="text-2xl font-bold text-blue-600">Luxury Bath DG</div>
```
Simply replace "Luxury Bath DG" with your desired company name.

### Phone Number Updates
The phone number appears in multiple locations. Update all instances:
```html
<!-- In header -->
<a href="tel:8775596432">(877) 559-6432</a>

<!-- In hero section -->
<a href="tel:8775596432">Call (877) 559-6432 Today!</a>

<!-- In contact section -->
<a href="tel:8775596432">Call (877) 559-6432</a>
```

### Modifying Tailwind Classes

#### Common Class Patterns:
- Text Colors: `text-{color}-{shade}` (e.g., `text-blue-600`)
- Background Colors: `bg-{color}-{shade}` (e.g., `bg-white`)
- Padding: `p-{size}`, `px-{size}`, `py-{size}` (e.g., `p-8`, `px-6`)
- Margin: `m-{size}`, `mx-{size}`, `my-{size}` (e.g., `mb-4`)
- Font Size: `text-{size}` (e.g., `text-xl`)

Example of updating a button's appearance:
```html
<!-- Original -->
<a href="tel:8775596432" class="bg-blue-600 text-white px-6 py-2 rounded-full">

<!-- Modified (darker blue, larger padding) -->
<a href="tel:8775596432" class="bg-blue-700 text-white px-8 py-3 rounded-full">
```

## Managing Navigation Links

### Internal Navigation
The page uses anchor links to scroll to sections. Update these in both the header and footer:

```html
<!-- In header navigation -->
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To add a new section:
1. Create your new section with an ID:
```html
<section id="new-section">
    <!-- Content here -->
</section>
```
2. Add the corresponding navigation link:
```html
<a href="#new-section" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">New Section</a>
```

### Email Link Updates
Update the email address in both the contact section and footer:
```html
<!-- In contact section -->
<a href="mailto:info@LuxuryBathDG.com">Email Us</a>

<!-- In footer -->
<p class="text-gray-400">info@LuxuryBathDG.com</p>
```

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your project directory:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Replace the placeholder links in the footer:
```html
<!-- Original footer links -->
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>

<!-- Updated footer links -->
<ul class="space-y-2">
    <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

### Step 3: Maintain Consistent Styling
Copy these elements from `index.html` to your new pages:
- The entire `<head>` section
- The header navigation
- The footer section

## Troubleshooting

### Common Issues and Solutions

1. **Broken Navigation Links**
   - Ensure section IDs match exactly with href attributes
   - Check for typos in href values
   - Verify file names match exactly for external pages

2. **Styling Problems**
   - Confirm Tailwind CDN is properly loaded
   - Check for missing or mistyped class names
   - Verify proper class order for responsive designs

3. **Layout Issues**
   - Check container classes are present (`container mx-auto px-6`)
   - Verify grid classes for responsive layouts
   - Ensure proper nesting of elements

### Need Help?
If you encounter issues:
1. Check the browser's developer tools (F12) for errors
2. Verify all files are in the correct directory
3. Ensure all links use the correct relative paths
4. Double-check class names against Tailwind documentation

Remember to test all changes across different device sizes using browser developer tools.