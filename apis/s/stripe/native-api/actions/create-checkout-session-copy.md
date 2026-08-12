# Create Variable-Amount Checkout Session with Stripe

Creates a new checkout session in Stripe.

## Endpoint

- **Method:** `POST`
- **Path:** `checkout/sessions`
- **Base URL:** `https://api.stripe.com/v1`
- **Official documentation:** [Create Variable-Amount Checkout Session](https://docs.stripe.com/api/checkout/sessions/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mode` | body | `list<string>` | yes | Checkout mode: payment, setup, or subscription. Accepted values: `payment`, `setup`, `subscription`. |
| `line_items[]` | body | `array<object>` | no | Line items for this checkout session. |
| `line_items[].quantity` | body | `number` | no | Quantity for the line item. |
| `success_url` | body | `string` | no | URL to redirect customers after successful checkout in hosted mode. |
| `return_url` | body | `string` | no | URL to return customers to your site for embedded/custom UI modes. |
| `cancel_url` | body | `string` | no | URL to redirect customers if they cancel checkout. |
| `customer` | body | `string` | no | Existing customer ID to prefill checkout. |
| `customer_email` | body | `string` | no | Email used to prefill customer data when no customer ID is provided. |
| `payment_method_types[]` | body | `array<string>` | no | Allowed payment method types for this session. |
| `ui_mode` | body | `list<string>` | no | Checkout UI mode: hosted, embedded, or custom. Accepted values: `custom`, `embedded`, `hosted`. |
| `client_reference_id` | body | `string` | no | Reference ID to reconcile session with your internal systems. |
| `price_data_currency` | body | `string` | yes | Three-letter lowercase currency code for the inline Stripe Price, for example usd. |
| `unit_amount` | body | `number` | yes | Positive integer amount in the currency's smallest unit (cents for USD). |
| `product_name` | body | `string` | yes | Customer-visible product or payment-request name. |
