# SocialBoost Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the SocialBoost landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name:**
```html
<div class="text-2xl font-bold bg-gradient-to-r from-blue-600 to-purple-600 bg-clip-text text-transparent">
    SocialBoost  <!-- Change this text -->
</div>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>  <!-- Update text here -->
    <a href="#benefits">Benefits</a>  <!-- Update text here -->
    <a href="#faq">FAQ</a>           <!-- Update text here -->
    <a href="#contact">Contact</a>    <!-- Update text here -->
</div>
```

### Hero Section
Located at the top of the page with the main headline:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-blue-600 to-purple-600 bg-clip-text text-transparent">
    Boost Local Sales with Smart Social Media Marketing  <!-- Update main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Top-Rated Social Media Marketing Agency Near You  <!-- Update subheading -->
</p>
```

### Tailwind CSS Classes Explained
- `text-4xl`: Large text size (mobile)
- `md:text-5xl`: Larger text on medium screens
- `lg:text-6xl`: Largest text on large screens
- `mb-8`: Margin bottom spacing
- `text-gray-600`: Text color
- `hidden md:flex`: Hidden on mobile, flex display on medium screens

## Managing Links

### Navigation Menu Links
Current internal links point to page sections:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update:
1. Identify the section ID you want to link to
2. Add a '#' before the ID
3. Ensure the ID exists in the corresponding section

### Call-to-Action Buttons
Located in multiple sections, update the href attribute:
```html
<a href="https://your-new-link-here.com"
   class="inline-block px-8 py-4 bg-blue-600 text-white rounded-full">
    Start Growing Your Business
</a>
```

### Footer Links
Located at the bottom of the page:
```html
<div class="grid grid-cols-1 md:grid-cols-4 gap-12">
    <!-- Quick Links Section -->
    <ul class="space-y-2">
        <li><a href="#features">Features</a></li>
        <li><a href="#benefits">Benefits</a></li>
        <li><a href="#faq">FAQ</a></li>
    </ul>
</div>
```

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your project directory:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Replace the placeholder links with actual page links:
```html
<!-- Before -->
<li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>

<!-- After -->
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

### Step 3: Maintain Consistent Styling
Copy these classes to maintain consistent link styling:
```html
class="text-gray-400 hover:text-white transition-colors duration-300"
```

## Troubleshooting

### Common Issues and Solutions

1. **Links Not Working**
   - Verify file names match exactly
   - Ensure files are in the same directory
   - Check for typos in href attributes

2. **Responsive Design Issues**
   - Keep the `md:` and `lg:` prefixed classes for proper scaling
   - Don't remove the `container` class from main sections
   - Maintain the existing grid structure in sections

3. **Gradient Text Not Showing**
   - Ensure all three classes are present:
     ```html
     bg-gradient-to-r from-blue-600 to-purple-600 bg-clip-text text-transparent
     ```

### Best Practices
- Always backup files before making changes
- Test all links after updating
- View changes on multiple screen sizes
- Keep the existing class structure for consistency
- Use browser developer tools to preview changes

For additional help or questions, refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs) or contact your development team.