# Update Checkout Page with Checkout Page

Updates a checkout page in Checkout Page.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/checkout-pages/:pageId`
- **Base URL:** `https://api.checkoutpage.com`
- **Official documentation:** [Update Checkout Page](https://checkoutpage.com/docs/api/v1/checkout-pages/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageId` | path | `string` | yes | The unique identifier of the checkout page. |
| `name` | body | `string` | no | Internal page name used in your dashboard and API responses. |
| `slug` | body | `string` | no | Page URL slug. For events and forms the slug defaults to the slugified version of your `title`. For checkouts the slug defaults to the slugified version of your `productData.title`. |
| `status` | body | `string` | no | Initial publication status. Defaults to "published" if not provided. |
| `locale` | body | `string` | no | Locale code. |
| `customizeCheckoutConfirmation` | body | `boolean` | no | If set to true `confirmationCheckoutMessage` and `confirmationCheckoutTitle` will be displayed on the confirmation page. Defaults to `false`. |
| `allowDynamicTitle` | body | `boolean` | no | Allow page title to be overridden via URL query parameters. |
| `allowDynamicDescription` | body | `boolean` | no | Allow page description to be overridden via URL query parameters. |
| `closePopupOnClickOutside` | body | `boolean` | no | Whether a popup embed closes when clicking outside the container. Defaults to `false`. |
| `redirect` | body | `object` | no | If enabled, redirects the customer to the specified URL before the page loads. |
| `afterPaymentAction` | body | `string` | no | Behavior after checkout. `confirmation` shows the confirmation page. `checkout` redirects to `redirectPageId`. `redirect` sends the customer to `redirectUrl`. Defaults to `confirmation`. |
| `confirmationCheckoutTitle` | body | `string` | no | Confirmation title. |
| `confirmationCheckoutMessage` | body | `string` | no | Confirmation message. Accepts HTML or plaintext. |
