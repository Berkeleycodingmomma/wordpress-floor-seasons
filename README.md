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


### Amelia Plugin Shortcode Integration:

```php
// Custom shortcode for Amelia booking form
function custom_amelia_booking() {
    return do_shortcode('[ameliabooking]');
}
add_shortcode('custom_amelia_booking', 'custom_amelia_booking');


