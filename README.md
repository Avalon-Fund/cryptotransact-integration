# MoonPay On-Ramp Integration for WordPress

This repository contains the integration for adding MoonPay's on-ramp service to your website. The integration allows users to buy cryptocurrency using MoonPay directly from your website.

## Features

- **MoonPay On-Ramp**: Allow your users to buy cryptocurrency through MoonPay's service.
- **Theme Toggle**: Easily switch between light and dark themes on your website.

## Installation

1. **Download the Integration Files**: Clone this repository or download the files from the `index.html`.
2. **Include the Files in Your WordPress Theme**: Add the `index.html` file to your WordPress theme's directory.

## Usage

1. **Add the HTML File**: Place the `index.html` file in the desired location within your WordPress theme.
2. **Customize the Button**: Update the button IDs and classes if necessary to match your website's styling.

## Example

Below is an example of the HTML structure used in this integration:

```html
<!DOCTYPE html>
<html lang="en" data-theme="light">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MoonPay On-Ramp - Web SDK</title>
    <link rel="stylesheet" href="https://crypto-transact.com/api/v1/payment/styles.css">
</head>
<body>
    <h1>MoonPay On-Ramp Integration - Web SDK</h1>
    <button id="startTransaction" class="moonpay-button">Buy with MoonPay</button>
    <button id="themeToggle" class="theme-toggle">Toggle Theme</button>

    <script type="module" src="https://crypto-transact.com/api/v1/payment/moonpay/script.js"></script>
    <script>
        const themeToggle = document.getElementById('themeToggle');
        const html = document.documentElement;
        
        themeToggle.addEventListener('click', () => {
            const currentTheme = html.getAttribute('data-theme');
            const newTheme = currentTheme === 'light' ? 'dark' : 'light';
            html.setAttribute('data-theme', newTheme);
        });
    </script>
</body>
</html>
