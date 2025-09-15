# Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the LoanPhone landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Main Sections Overview
The landing page is divided into these key sections:
- Header (navigation)
- Hero section
- Features section
- Benefits section
- Call-to-action section
- Footer

### Updating Text Content

#### Hero Section
Located near the top of the page, find this code:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight text-gray-900 mb-6">
    How to Use a Car Loan Calculator to Save Money on Your Next Vehicle Purchase
</h1>
```
To update:
1. Locate the text between the `<h1>` tags
2. Replace with your new heading
3. Keep the existing classes to maintain styling

#### Features Section
Find the feature cards starting with:
```html
<div class="bg-white p-8 rounded-xl shadow-lg hover:shadow-xl transition-all duration-300">
    <h3 class="text-xl font-semibold mb-4">Specialist Bad-Credit Lender Panel</h3>
    <p class="text-gray-600">Access our network of specialized lenders...</p>
</div>
```
To update feature cards:
1. Locate each card within the features section
2. Update the `<h3>` title text
3. Modify the `<p>` description text
4. Keep all existing classes

### Understanding Tailwind Classes

Key class patterns used throughout:
- Spacing: `px-4`, `py-24`, `mb-6` (padding and margins)
- Text sizes: `text-xl`, `text-2xl`, `text-4xl`
- Colors: `text-gray-600`, `bg-blue-600`
- Responsive design: `md:text-5xl`, `lg:text-6xl`

Example of modifying responsive text size:
```html
<!-- Original -->
<h1 class="text-4xl md:text-5xl lg:text-6xl">

<!-- Making text smaller -->
<h1 class="text-3xl md:text-4xl lg:text-5xl">
```

## Fixing Broken Links

### Current Link Inventory
Navigation menu links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="https://tinyurl.com/ym68y8f2">Get Started</a>
```

To update any link:
1. Locate the `<a>` tag
2. Modify the `href` attribute
3. Update the text between the tags if needed

### Internal Links
For sections on the same page:
```html
<!-- Format -->
<a href="#section-id">Section Name</a>

<!-- Example -->
<a href="#features">Features</a>
```

### External Links
For links to other websites:
```html
<!-- Format -->
<a href="https://full-website-url">Link Text</a>

<!-- Example -->
<a href="https://your-calculator-url.com">Calculate Your Loan</a>
```

## Linking Privacy and Terms Pages

### Adding Privacy Policy Link
Locate this section in the footer:
```html
<div>
    <h3 class="text-white text-lg font-semibold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
```

Update the privacy policy link:
```html
<li><a href="/privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
```

### Adding Terms of Service Link
In the same footer section:
```html
<li><a href="/terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

### Maintaining Consistent Styling
When adding new links, copy these classes:
```html
class="hover:text-white transition-colors duration-300"
```

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
   - Ensure section IDs match exactly (case-sensitive)
   - Check for extra spaces in IDs
   - Verify the `#` symbol before section IDs

2. **Responsive Design Issues**
   - Keep all responsive classes (`md:`, `lg:` prefixes)
   - Test on different screen sizes
   - Don't remove container classes: `container mx-auto`

3. **Styling Inconsistencies**
   - Copy existing classes for similar elements
   - Maintain the same color schemes (blue-600, gray-600, etc.)
   - Keep hover effects: `hover:` classes

Remember to:
- Test all changes in multiple browsers
- Verify mobile responsiveness
- Back up your code before making changes
- Maintain consistent indentation
- Keep the original class structure

For additional help, consult the [Tailwind CSS documentation](https://tailwindcss.com/docs) or reach out to your development team.