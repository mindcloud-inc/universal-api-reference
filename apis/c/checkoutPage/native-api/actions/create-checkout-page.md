# Create Checkout Page with Checkout Page

Creates a checkout page in Checkout Page.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/checkout-pages/`
- **Base URL:** `https://api.checkoutpage.com`
- **Official documentation:** [Create Checkout Page](https://checkoutpage.com/docs/api/v1/checkout-pages/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Internal page name used in your dashboard and API responses. |
| `slug` | body | `string` | no | Page URL slug. For events and forms the slug defaults to the slugified version of your `title`. For checkouts the slug defaults to the slugified version of your `productData.title`. |
| `status` | body | `string` | no | Initial publication status. Defaults to "published" if not provided. |
| `productData` | body | `object` | no | Product configuration for checkout pages.  Use this object to define pricing mode, subscription/payment plan behavior, inventory, variants, and conditional variant visibility.  Common setup patterns: - Standard one-time checkout: set `price.amount`, `price.currency`, and keep `price.pricingType` as `single`. - Variant-driven pricing: set `price.pricingType` to `multiple`, then define `variants` and per-option `additionalChargeAmount`. - Subscriptions (recurring): configure `price.recurring`. - Payment plans (fixed installments): configure `price.paymentPlan` with `planIterations`.  Important rules: - You cannot set both `price.recurring` and `price.paymentPlan`. - `price.payWhatYouWant` cannot be used with subscriptions or payment plans. - `trialPeriodDays` and `startDate` are mutually exclusive within `recurring` and `paymentPlan`. - For conditional variant logic (`showHideLogic`) or `preselect`, set a `key` on variants/options to enable cross-references. Keys are not persisted. |
| `fields[]` | body | `array<object>` | no | Custom checkout fields to create. If one of your fields must be an `email` element and `required` must be true. Defaults to a name and email field if none are set. |
| `locale` | body | `string` | no | Locale code. |
| `customizeCheckoutConfirmation` | body | `boolean` | no | If set to true `confirmationCheckoutMessage` and `confirmationCheckoutTitle` will be displayed on the confirmation page. Defaults to `false`. |
| `allowDynamicTitle` | body | `boolean` | no | Allow page title to be overridden via URL query parameters. |
| `allowDynamicDescription` | body | `boolean` | no | Allow page description to be overridden via URL query parameters. |
| `closePopupOnClickOutside` | body | `boolean` | no | Whether a popup embed closes when clicking outside the container. Defaults to `false`. |
| `redirect` | body | `object` | no | If enabled, redirects the customer to the specified URL before the page loads. |
| `afterPaymentAction` | body | `string` | no | Behavior after checkout. `confirmation` shows the confirmation page. `checkout` redirects to `redirectPageId`. `redirect` sends the customer to `redirectUrl`. Defaults to `confirmation`. |
