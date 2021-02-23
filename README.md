# README

# Contents

- Introduction
- Prerequisites
- Rebranding
- Installing the payment module
- License

# Introduction

This Woo-Commerce module provides an easy method to integrate with the payment gateway.
 - The woocommerce-latest directory contains the files that need to be uploaded to the wp-content/plugins/ directory
 - Supports WooCommerce versions: **3.2 - 4.7**

# Prerequisites

- The module requires the following prerequisites to be met in order to function correctly:
    - Woo-commerce Wordpress extension
    - The 'bcmath' php extension module: https://www.php.net/manual/en/book.bc.php

> Please note that we can only offer support for the Module itself. While every effort has been made to ensure the payment module is complete and bug free, we cannot guarantee normal functionality if unsupported changes are made.

# Rebranding

In order to successfully rebrand this module, please complete the following updates:

In `Woocommerce-Payment-Network.php` change the following to match your brand

1. Line 7 to reflect your brand
2. Line 8 to reflect your own domain
3. Line 12 to reflect your support details
4. Line 74 replace PaymentNetwork in the admin_url with your $gateway (as below, with no spaces)

In file `includes/class-wc-payment-network.php` change the following to match that you've been provided:

```
    const MMS_URL                  = 'https://example.domain.com';
    const DEFAULT_HOSTED_URL       = 'https://example.domain.com/hosted/';
    const DEFAULT_HOSTED_MODAL_URL = 'https://example.domain.com/hosted/modal/';
    const DEFAULT_DIRECT_URL       = 'https://example.domain.com/direct/';
    const DEFAULT_MERCHANT_ID      = '100001';
    const DEFAULT_SECRET           = 'Circle4Take40Idea';
```

and update this field to represent your brand name

```
    private $gateway     = 'PaymentNetwork';
```

When downloading as a zip file, you can right-click and rename to remove the `Unbranded` text from the filename.

# Installing and configuring the module

1. Unzip and upload the plugin folder to your /wp-content/plugins/ directory or navigate to Plugins -> add new plugin -> upload plugin and then drop the zip file where specified
2. Activate the plugin through the Plugins menu in WordPress
3. Go to WooCommerce -> Plugins -> Payment-Network and click on the 'settings' button
4. Enter your MerchantID / Secretkey and update the customer/country code
5. If you own a custom form on your gateway, enter the full URL to it in the custom form box (Including trailing /)
6. Selects what type of integration you would like to use
7. Set the Enabled option to true
8. Click 'Save Changes'

License
----
MIT
