# Daytime Tutoring Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Daytime Tutoring landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company name and navigation menu.

```html
<!-- To update company name -->
<div class="text-2xl font-bold text-gray-800">Daytime Tutoring</div>
```

To modify:
1. Locate this div in the header section
2. Change "Daytime Tutoring" to your desired text
3. Adjust text size using Tailwind classes:
   - `text-xl` (smaller)
   - `text-2xl` (current size)
   - `text-3xl` (larger)

### Hero Section
The main banner section includes the headline and call-to-action button.

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-8 leading-tight">
    Daytime Tutor Caterham
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12 leading-relaxed">
    Empowering students through personalized education and dedicated support
</p>
```

To modify:
1. Update headline text between `<h1>` tags
2. Modify subheading text in the `<p>` tag
3. Common Tailwind classes explained:
   - `md:text-5xl`: Applies font size on medium screens
   - `mb-8`: Adds margin bottom spacing
   - `leading-tight`: Controls line height

### Features Section
Each feature card can be customized:

```html
<div class="bg-white rounded-xl shadow-lg p-8 hover:shadow-xl transition-shadow duration-300">
    <h3 class="text-xl font-semibold mb-4">Individual Attention</h3>
    <p class="text-gray-600 leading-relaxed">Personalized one-on-one attention...</p>
</div>
```

To modify:
1. Locate the feature cards in the features section
2. Update heading text in `<h3>` tags
3. Modify description text in `<p>` tags
4. Adjust styling using Tailwind classes:
   - `shadow-lg`: Adds shadow effect
   - `p-8`: Adds padding
   - `rounded-xl`: Rounds corners

## Fixing Broken Links

### Navigation Menu Links
Current navigation links are internal anchors:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update:
1. For internal links (same page):
   - Use `#section-name` format
   - Ensure section IDs match exactly
2. For external links:
   - Replace `#section-name` with full URL
   - Example: `href="https://example.com/page"`

### Email Links
Update the email address in two locations:

```html
<!-- Contact section -->
<a href="mailto:test@email.com">test@email.com</a>

<!-- Footer section -->
<p class="text-gray-400">Email: test@email.com</p>
```

To modify:
1. Replace `test@email.com` with your actual email
2. Update both the visible text and `mailto:` link

## Linking Privacy and Terms Pages

### Footer Legal Links
Current placeholder links for legal pages:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
   - Verify that section IDs match navigation href attributes exactly
   - Check for typos in both the link and section ID
   - Section IDs are case-sensitive

2. **Responsive Design Issues**
   - Check that you're maintaining responsive classes (e.g., `md:text-5xl`)
   - Test on different screen sizes using browser dev tools
   - Don't remove `container` and `mx-auto` classes

3. **Styling Problems**
   - Keep the `transition-colors duration-300` classes for smooth hover effects
   - Maintain the existing padding/margin classes for proper spacing
   - Don't remove `hover:` classes as they provide interactive effects

Remember to:
- Always test changes in multiple browsers
- Maintain the existing responsive design structure
- Keep consistent spacing and styling across sections
- Back up your files before making significant changes

Need more help? Refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs) for detailed class information.