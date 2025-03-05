# Plumbing Landing Page Maintenance Guide

This guide will help you maintain and customize the plumbing services landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your company name and navigation menu. To update:

1. **Company Name:**
```html
<!-- Find this line in the header section -->
<div class="text-2xl font-bold text-blue-600">Plumber Pro</div>
```
Simply replace "Plumber Pro" with your company name.

### Hero Section
Located at the top of the page with the main headline:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6 text-gray-900">
    Reliable Plumbing Solutions, Done Right the First Time!
</h1>
```
- Replace the text between the `<h1>` tags
- The classes ensure responsive text sizing:
  - `text-4xl`: Default size
  - `md:text-5xl`: Medium screens
  - `lg:text-6xl`: Large screens

### Tailwind CSS Class Guide
Common classes used throughout:
- Text colors: `text-gray-600`, `text-blue-600`, `text-white`
- Background colors: `bg-white`, `bg-blue-600`, `bg-gray-50`
- Spacing: `px-6` (padding left/right), `py-4` (padding top/bottom), `mb-4` (margin bottom)
- Hover effects: `hover:bg-blue-700`, `hover:scale-105`

To modify styles, adjust these classes directly in the HTML elements.

## Managing Links

### Navigation Menu Links
Current navigation links are found in the header:
```html
<div class="hidden md:flex space-x-8">
    <a href="#services" class="text-gray-600 hover:text-blue-600 transition duration-300">Services</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600 transition duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600 transition duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-blue-600 transition duration-300">Contact</a>
</div>
```

To update links:
1. Locate the `<a>` tag you want to modify
2. Change the `href` attribute:
   - Internal sections: Use `#section-name`
   - External pages: Use full URL (e.g., `https://example.com`)

### Call-to-Action Links
The "Book Now" and "Schedule Service" buttons currently point to Google:
```html
<a href="https://google.com" class="bg-blue-600 text-white px-6 py-2 rounded-full">Book Now</a>
```
Replace `https://google.com` with your booking system URL.

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your project directory:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Locate the legal section in the footer:
```html
<div>
    <h3 class="text-xl font-bold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-blue-400 transition duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-blue-400 transition duration-300">Terms of Service</a></li>
    </ul>
</div>
```

Replace the `#` placeholders:
```html
<li><a href="privacy.html" class="hover:text-blue-400 transition duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-blue-400 transition duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure section IDs match the href attributes
   - Check for typos in IDs
   - Verify that sections have the correct ID attribute

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - Keep the viewport meta tag in the head section
   - Test on different screen sizes using browser dev tools

3. **Style Changes Not Working**
   - Verify Tailwind CDN link is working
   - Check for typos in class names
   - Ensure classes are space-separated

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Use browser developer tools (F12) to inspect elements
- Test all links after making changes
- Maintain backup copies before making major changes

Remember to always test your changes across different devices and browsers to ensure consistency.