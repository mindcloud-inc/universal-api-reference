# Create Event with Checkout Page

Creates a event in Checkout Page.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/events/`
- **Base URL:** `https://api.checkoutpage.com`
- **Official documentation:** [Create Event](https://checkoutpage.com/docs/api/v1/events/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Internal page name used in your dashboard and API responses. |
| `title` | body | `string` | no | Public title shown to customers on the page. |
| `slug` | body | `string` | no | Page URL slug. For events and forms the slug defaults to the slugified version of your `title`. For checkouts the slug defaults to the slugified version of your `productData.title`. |
| `description` | body | `string` | no | Page description shown to customers. Accepts HTML or plain text. |
| `status` | body | `string` | no | Initial publication status. Defaults to "published" if not provided. |
| `fields[]` | body | `array<object>` | no | Custom checkout fields to create. If one of your fields must be an `email` element and `required` must be true. Defaults to a name and email field if none are set. |
| `locale` | body | `string` | no | Locale code. |
| `customizeCheckoutConfirmation` | body | `boolean` | no | If set to true `confirmationCheckoutMessage` and `confirmationCheckoutTitle` will be displayed on the confirmation page. Defaults to `false`. |
| `allowDynamicTitle` | body | `boolean` | no | Allow page title to be overridden via URL query parameters. |
| `allowDynamicDescription` | body | `boolean` | no | Allow page description to be overridden via URL query parameters. |
| `closePopupOnClickOutside` | body | `boolean` | no | Whether a popup embed closes when clicking outside the container. Defaults to `false`. |
| `redirect` | body | `object` | no | If enabled, redirects the customer to the specified URL before the page loads. |
