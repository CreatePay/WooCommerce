# CreatePay for WooCommerce

A payment module for WooCommerce that enables customers to pay for their orders using the Cardstream hosted payment form or direct payment gateway.

## Requirements

- **WooCommerce:** Version 10.x
- **WordPress:** Up to version 7.x
- **PHP:** BCMath extension

## Configuration Requirements

To configure the module, you will need the following:

- Merchant ID
- Signature/Secret Key
- Gateway URL

If you already have a CreatePay account, please contact [createcommerce@createpay.com](mailto:createcommerce@createpay.com).

For all other enquiries, please contact [hello@createpay.com](mailto:hello@createpay.com).

## Features

The CreatePay WooCommerce module allows customers to pay for their orders using the Cardstream payment gateway.

Supported payment methods include:

- **Card:** Displays card payment fields directly on the WooCommerce checkout page.
- **Hosted:** Redirects customers to a separate checkout page containing the hosted payment form in an iframe.
- **Apple Pay:** Supports Apple Pay payments, subject to the required configuration.

## Installation

### Option 1: Install via the WordPress Admin Panel

1. Download the ZIP file containing the `createpay` plugin folder.
2. Log in to your WordPress admin panel.
3. Navigate to **Plugins > Add New**.
4. Click **Upload Plugin**.
5. Click **Choose File** and select the downloaded ZIP file.
6. Click **Install Now**.
7. Once installation is complete, click **Activate Plugin**.

### Option 2: Manual Installation

1. Extract the downloaded ZIP file.
2. Upload the `createpay` plugin folder to your WordPress installation's `wp-content/plugins/` directory.
3. Log in to your WordPress admin panel.
4. Navigate to **Plugins**.
5. Locate the CreatePay plugin and click **Activate**.

## Configuration

Once the plugin has been installed and activated, follow these steps to configure it.

### 1. Configure the Main Settings

1. Navigate to **WooCommerce > CreatePay** in your WordPress admin panel.
2. Enter the following details:
   - **Merchant ID:** Your CreatePay merchant ID.
   - **Security Key:** Your CreatePay security key.
   - **Country Code:** Enter `826` for the United Kingdom.
3. Leave the **Payment Gateway** setting unchanged.
4. Click **Save Changes**.

### 2. Configure Payment Methods

Navigate to the **Payment Methods** section of the plugin settings.

Choose the payment method you want to enable:

| Payment Method | Description |
| --- | --- |
| Card | Displays card payment fields directly on the WooCommerce checkout page. |
| Hosted | Displays the hosted payment form on a separate page after checkout, using an iframe. |
| Hosted Fields | Displays the hosted payment fields within the iframe. |

Enable the required payment method and click **Save Changes**.

### 3. Configure Apple Pay

To enable Apple Pay, you must configure your domain and upload the required verification file.

#### Step 1: Download the CSR

1. Navigate to the [CreatePay Dashboard](https://dashboard.createpay.com/).
2. Log in using the credentials provided to you.
3. Navigate to **Preferences > Digital Wallets**.
4. Locate the hyperlink to download the CSR, just above **Update Apple Pay Preferences**.
5. Download the CSR file.

#### Step 2: Configure Apple Pay in WooCommerce

1. Open the downloaded CSR file.
2. Copy its contents.
3. Return to your WordPress admin panel.
4. Navigate to **WooCommerce > CreatePay**.
5. Locate the Apple Pay settings.
6. Paste the copied content into the appropriate Apple Pay and **Domain Verification File** fields.
7. Click **Save Changes**.

#### Step 3: Verify Your Domain

1. Return to the [CreatePay Dashboard](https://dashboard.createpay.com/).
2. Navigate to **Preferences > Digital Wallets**.
3. Enter your website URL exactly as it appears at the root level of your domain.
4. Click **Save**.
5. When the confirmation popup appears, click **OK**.

The dashboard will check whether the domain verification file is present and accessible on your website.

If verification is successful, a green tick will appear at the top of the page.

## Troubleshooting

### Apple Pay Domain Verification Fails

**Problem:** No green tick appears in the CreatePay Dashboard after entering your website URL.

**Solution:**

1. Check that the website URL has been entered correctly.
2. Ensure the URL matches your domain configuration, including whether or not it uses `www`.
3. Open the following URL in your browser, replacing `{WEBSITE_URL}` with your actual website address:

   ```text
   https://{WEBSITE_URL}/.well-known/apple-developer-merchantid-domain-association
   ```

4. Verify that the contents of the domain verification file are displayed.

If the file is not accessible:

- Check that the file has been uploaded and configured correctly.
- Ensure that your web server is not blocking access to the file.
- Verify that the file can be accessed publicly at the specified URL.

If the problem persists, contact CreatePay Support.

### Refund Error: Transaction Is Not in a Refundable State

**Problem:** The following error appears when attempting to process a refund through the WooCommerce module:

`Transaction is not in a refundable state`

**Solution:**

1. Log in to the [CreatePay Dashboard](https://dashboard.createpay.com/).
2. Navigate to **Preferences > Credentials > Direct Integration**.
3. Enter your server's IP address.
4. Save the changes and try processing the refund again.

If the issue persists, contact CreatePay Support.

---

## Support

For assistance with an existing CreatePay account or technical support, contact:

- **Existing CreatePay accounts:** [createcommerce@createpay.com](mailto:createcommerce@createpay.com)
- **General enquiries:** [hello@createpay.com](mailto:hello@createpay.com)
