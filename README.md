# floorseasonsutah.com

**License:** MIT Open Source Initiative

## Description:
Floor Seasons Utah is a custom WordPress website designed for a floor cleaning business. The website integrates the Kadence Theme for fully customizable design and the Amelia Booking Plugin for seamless appointment scheduling. The site allows users to view available services and easily schedule appointments online. The frontend design was completely customized using PHP, HTML, and CSS to meet the client's business needs, creating a user-friendly and professional online presence.



## Overview
### The Challenge:
The primary objective was to create a WordPress website for Floor Seasons Utah that is easy to use for customers booking floor cleaning services. The website needed to offer user-friendly navigation and booking functionality. The Kadence Theme was used as the base theme, which was then stripped down and redesigned for the specific needs of the client. Amelia, a booking plugin, was integrated to handle online appointment scheduling seamlessly.

## Requirements for the Project:
- WordPress installation for the base platform.
- Kadence Theme used for creating a responsive and customizable website layout.
- Amelia Plugin for appointment booking and scheduling functionality.
- Customization of PHP files, CSS, and HTML to adapt the theme and plugin to meet client requirements.
- Use PHP for backend functionality such as customizing theme templates and integrating plugins.
- Design and develop the frontend to reflect the branding and business services of Floor Seasons Utah.

## Built With:
- **WordPress**: Platform used for content management.
- **Kadence Theme**: Theme used for the design layout and customization. [Kadence Theme Website](https://www.kadencewp.com)
- **Amelia Plugin**: Plugin used for appointment scheduling. [Amelia Plugin Website](https://wpamelia.com)
- **PHP**: Backend language for customizing theme and plugin.
- **HTML/CSS**: Used for front-end design and styling.
- **JavaScript**: For interactivity in certain sections.
- **DreamHost**: Hosting provider. [DreamHost Website](https://www.dreamhost.com)

## Code Snippets of our project:
### Customizing the Kadence Theme Header with PHP:
```php
// Add custom code to Kadence theme's header
function custom_header_code() {
    echo '<div class="custom-header">Welcome to Floor Seasons Utah!</div>';
}
add_action('kadence_header', 'custom_header_code');
```
#

### Amelia Plugin Shortcode Integration:
```php
// Custom shortcode for Amelia booking form
function custom_amelia_booking() {
    return do_shortcode('[ameliabooking]');
}
add_shortcode('custom_amelia_booking', 'custom_amelia_booking');

```
ABOVE: This shortcode integrates the Amelia booking plugin into a custom page or post on the WordPress site, allowing users to book appointments directly through the website.
#

### Custom CSS to modify styles for a specific page
```php
function custom_page_styles() {
    if (is_page('services')) {
        echo '<style>
            .page-title { font-size: 30px; color: #333; }
            .service-list { margin-top: 20px; }
        </style>';
    }
}
add_action('wp_head', 'custom_page_styles');
```
ABOVE: This snippet customizes the styles for the "Services" page by targeting specific elements like the page title and the service list. It ensures that the page has a unique look while maintaining the overall theme's integrity.
#
### Customize the hero section text and background image
```php
function custom_hero_section() {
    if (is_front_page()) {
        echo '<div class="hero-section" style="background-image: url(\'/path/to/custom-image.jpg\');">
            <h1>Welcome to Floor Seasons Utah</h1>
            <p>Your trusted partner in floor cleaning services.</p>
        </div>';
    }
}
add_action('wp_head', 'custom_hero_section');
```
ABOVE: This code snippet customizes the hero section on the homepage, setting a unique background image and adding custom text that welcomes visitors and highlights the business.
#
### Add a contact form to the footer section of the website
```php
function custom_contact_form() {
    echo '<div class="footer-contact-form">
        <h3>Contact Us</h3>
        <form action="/submit-form" method="POST">
            <input type="text" name="name" placeholder="Your Name" required>
            <input type="email" name="email" placeholder="Your Email" required>
            <textarea name="message" placeholder="Your Message" required></textarea>
            <button type="submit">Submit</button>
        </form>
    </div>';
}
add_action('kadence_footer', 'custom_contact_form');
```
ABOVE: This snippet adds a custom contact form to the footer section of the website. It includes fields for name, email, and a message, providing a simple way for users to contact the business directly.
#
### Add Google Analytics script to the footer
```php
function google_analytics_script() {
    echo '<script async src="https://www.googletagmanager.com/gtag/js?id=UA-XXXXXXXXX-X"></script>';
    echo '<script>
        window.dataLayer = window.dataLayer || [];
        function gtag(){dataLayer.push(arguments);}
        gtag(\'js\', new Date());
        gtag(\'config\', \'UA-XXXXXXXXX-X\');
    </script>';
}
add_action('wp_footer', 'google_analytics_script');
```
ABOVE: This code snippet adds Google Analytics tracking code to the footer of the website. It enables you to track website performance and user behavior for analytics purposes.
#
### Redirect users to a thank you page after booking an appointment
```php
function redirect_after_appointment_booking() {
    if (is_page('thank-you')) {
        wp_redirect(home_url('/thank-you'));
        exit;
    }
}
add_action('template_redirect', 'redirect_after_appointment_booking');
```
ABOVE: This snippet redirects users to a "Thank You" page after they book an appointment, improving the user experience by confirming their action and providing next steps.
#

### Learned:
Throughout the project, several key lessons were learned that enhanced both my WordPress and PHP development skills:

#### Custom Theme Development:
While Kadence offers a flexible starting point, customizing it to fit specific needs required deep knowledge of PHP and WordPress theme structure. I learned how to modify core theme files and ensure that customizations were compatible with the theme’s built-in features.

#### Plugin Integration:
Integrating the Amelia plugin was straightforward, but ensuring it blended seamlessly into the theme required additional CSS and PHP adjustments. I also learned to work with WordPress shortcodes to embed dynamic booking functionality.

#### Optimizing User Experience:
Creating a user-friendly interface for the booking system was crucial. I focused on making the process intuitive, from selecting services to confirming appointments. Streamlining the user flow improved customer satisfaction and helped the business maintain efficiency.

#### Backend Customization:
While I didn't need to make deep backend changes, I worked with various PHP hooks to integrate the frontend booking system with the backend functionality of the plugin, ensuring everything worked smoothly. This project enhanced my understanding of WordPress's architecture and the importance of maintaining compatibility with plugins.

### License & Copyright ©:
License: MIT Open Source Initiative Link

Copyright © 2023 A&A Software Innovations

MIT License

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

### Authors:
[Amanda Gray & Austin Zumbro] - Project Developers  
[Client, Carey Elder] - Owner of Floor Seasons Utah




