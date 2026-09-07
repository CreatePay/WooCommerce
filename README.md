Setting up the module requires at a minimum a merchantID, a signature/secret key and a gateway URL. If you already have a CreatePay account please contact createcommerce@createpay.com. For all other enquires please contact hello@createpay.com



# WooCommerce
Payment module for WooCommerce



COMPATIBILITY
Compatible with version 10.x of WooCommerce and upto 7.x of Wordpress.

REQUIREMENTS
PHP-BCMaths

INTRODUCTION
This module enables the WooCommerce customers to pay for their items using the Cardstream hosted form or direct payment gateway.

What does it do?
Presents the option to pay with credit card or debit card via the Cardstream payment gateway.

INSTALLATION
Go to the plugins section of the admin panel

Click Add New

Click Upload plugin (Near the top left of the page next to the menu)

Click the "Choose File" button and select the module (which will be the whole zip file this readme is in)

Click the "Install Now" button and then click the "Activate" button

Go to your plugin settings which can be found at WooCommerce > CreatePay

In the main plugin settings, enter your Merchant ID, Security Key and Country Code (826 for UK). 

Leave Payment Gateway as it is

Save changes

Go to Payment Methods

For Card Fields to appear on the Checkout Page, enable payment method 'Card' and save

For Card Fields to appear on separate page after Checkout page (iframe), enable 'Hosted' and save

To enable ApplePay you will need to navigate to dashboard.createpay.com and log in with your username and password provided

Once logged in you will need to go to Preferences > Digital Wallets

Just above "Update Apple Pay Preferences" you will see a hyperlink to download our CSR

Once downloaded open the file, Copy and Paste the content into the plugin under ApplePay and in Domain Verification File

Save changes

Go back to dashboard.createpay.com and in Preferences > Digital Wallets, enter your website URL (exactly as it appears at root level) and click Save

When the popup appears, click OK. This will verify the Domain Verification File is present and accessible on your site with a Green Tick message at the top of the page

----------------------

Manual installation
Unzip and upload the plugin folder to your /wp-content/plugins/ directory

Activate the plugin through the Plugins menu in WordPress

Go to your plugin settings which can be found at WooCommerce > CreatePay

In the main plugin settings, enter your Merchant ID, Security Key and Country Code (826 for UK). 

Leave Payment Gateway as it is

Save changes

Go to Payment Methods

For Card Fields to appear on the Checkout Page, enable payment method 'Card' and save

For Card Fields to appear on separate page after Checkout page (iframe), enable 'Hosted' and save

To enable ApplePay you will need to navigate to dashboard.createpay.com and log in with your username and password provided

Once logged in you will need to go to Preferences > Digital Wallets

Just above "Update Apple Pay Preferences" you will see a hyperlink to download our CSR

Once downloaded open the file, Copy and Paste the content into the plugin under ApplePay and in Domain Verification File

Save changes

Go back to dashboard.createpay.com and in Preferences > Digital Wallets, enter your website URL (exactly as it appears at root level) and click Save

When the popup appears, click OK. This will verify the Domain Verification File is present and accessible on your site with a Green Tick message at the top of the page

----------------------

Troubleshooting
Problem: No Green Tick message shows in dashboard.createpay.com after entering URL
Solution: Ensure URL is entered exactly (with or without www. depending on domain setup). Go to {WEBSITE URL}/.well-known/apple-developer-merchantid-domain-association - this should show the contents of the file. If it does not show, ensure nothing at Server level is blocking access to the file being read. If problem persists, contact CreatePay Support

Problem: Error message - Transaction is not in a refundable state when trying to process a refund through the WooCommerce module
Solution: You will need to access Dashboard.createpay.com, Navigate to preferences, Credentials, Direct integration - Here you will need to put the IP address of your server. If the issue persists contact CreatePay Support
