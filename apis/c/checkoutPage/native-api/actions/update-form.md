# Update Form with Checkout Page

Updates a form in Checkout Page.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/forms/:pageId`
- **Base URL:** `https://api.checkoutpage.com`
- **Official documentation:** [Update Form](https://checkoutpage.com/docs/api/v1/forms/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageId` | path | `string` | yes | The unique identifier of the form page. |
| `name` | body | `string` | no | Internal page name used in your dashboard and API responses. |
| `title` | body | `string` | no | Public title shown to customers on the page. |
| `slug` | body | `string` | no | Page URL slug. For events and forms the slug defaults to the slugified version of your `title`. For checkouts the slug defaults to the slugified version of your `productData.title`. |
| `description` | body | `string` | no | Page description shown to customers. Accepts HTML or plain text. |
| `status` | body | `string` | no | Initial publication status. Defaults to "published" if not provided. |
| `locale` | body | `string` | no | Locale code. |
| `customizeCheckoutConfirmation` | body | `boolean` | no | If set to true `confirmationCheckoutMessage` and `confirmationCheckoutTitle` will be displayed on the confirmation page. Defaults to `false`. |
| `allowDynamicTitle` | body | `boolean` | no | Allow page title to be overridden via URL query parameters. |
| `allowDynamicDescription` | body | `boolean` | no | Allow page description to be overridden via URL query parameters. |
| `closePopupOnClickOutside` | body | `boolean` | no | Whether a popup embed closes when clicking outside the container. Defaults to `false`. |
| `redirect` | body | `object` | no | If enabled, redirects the customer to the specified URL before the page loads. |
| `afterPaymentAction` | body | `string` | no | Behavior after checkout. `confirmation` shows the confirmation page. `checkout` redirects to `redirectPageId`. `redirect` sends the customer to `redirectUrl`. Defaults to `confirmation`. |
