# 101Headshots Landing Page Maintenance Guide

This guide will help you maintain and customize the 101Headshots landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Main Sections Overview
The landing page is divided into these key sections:
- Header (Navigation)
- Hero Section
- Features Section
- Benefits Section
- FAQ Section
- Call-to-Action Section
- Footer

### Updating Text Content

#### Header Text
To update the company name in the header, locate this line:
```html
<a href="/" class="text-2xl font-bold text-gray-900">101Headshots</a>
```
Simply replace "101Headshots" with your desired text.

#### Hero Section
Find the hero section text within:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold tracking-tight text-gray-900 mb-6">
    Liberty, Missouri Corporate Headshot Photography Services
</h1>
<p class="text-xl md:text-2xl text-gray-600 max-w-3xl mx-auto mb-12">
    Transforming Liberty's leaders into confident visual communicators.
</p>
```
Replace the text while keeping the HTML tags intact.

### Modifying Tailwind CSS Classes

#### Understanding Responsive Classes
In this template, responsive classes use these prefixes:
- `md:` - applies to medium screens (768px and up)
- `lg:` - applies to large screens (1024px and up)

Example:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl">
```
This means:
- Mobile: text-4xl (2.25rem)
- Tablet: text-5xl (3rem)
- Desktop: text-6xl (3.75rem)

#### Common Tailwind Classes Used
- Text sizes: `text-sm`, `text-base`, `text-lg`, `text-xl`, etc.
- Colors: `text-gray-900`, `bg-blue-600`, `text-white`
- Spacing: `px-4`, `py-24`, `mb-6`, `mt-12`
- Flex layout: `flex`, `items-center`, `justify-between`

## Fixing Broken Links

### Current Link Inventory
1. Navigation Menu Links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="https://www.101headshots.com">Book Now</a>
```

2. Call-to-Action Links:
```html
<a href="https://www.101headshots.com">Schedule Your Session</a>
```

### Updating Links
1. For internal section links (starting with #):
   - Ensure the href matches the section ID
   - Example: `href="#features"` should match `id="features"`

2. For external links:
   - Replace the placeholder URL with your actual URL
   - Example:
   ```html
   <!-- Before -->
   <a href="https://www.101headshots.com">
   <!-- After -->
   <a href="https://www.yournewdomain.com">
   ```

## Linking Privacy and Terms Pages

### Adding Privacy Policy Link
Locate this section in the footer:
```html
<div>
    <h3 class="text-lg font-semibold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

Replace the # with your actual page paths:
```html
<li><a href="/privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="/terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Check that section IDs match exactly with href attributes
   - IDs are case-sensitive
   ```html
   <!-- Correct -->
   <section id="features">
   <a href="#features">
   
   <!-- Wrong -->
   <section id="Features">
   <a href="#features">
   ```

2. **Responsive Design Issues**
   - Ensure you're maintaining the responsive classes (md: and lg: prefixes)
   - Test on multiple screen sizes after making changes
   - Don't remove container classes (`max-w-7xl mx-auto px-4`)

3. **Styling Inconsistencies**
   - Keep the existing color scheme using Tailwind's color classes
   - Maintain padding and margin patterns throughout sections
   - Use the same transition classes for interactive elements:
     ```html
     class="transition-colors duration-300"
     ```

Remember to always test your changes across different devices and browsers after making updates.