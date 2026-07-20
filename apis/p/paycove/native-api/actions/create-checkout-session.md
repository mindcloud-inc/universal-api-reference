# Create Checkout Session with Paycove

Creates a checkout session in Paycove.

## Endpoint

- **Method:** `POST`
- **Path:** `https://paycove.io/api/checkout/:aid`
- **Base URL:** `https://paycove.io/api/v1`
- **Official documentation:** [Create Checkout Session](https://docs.paycove.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `aid` | path | `string` | yes | The account identifier for the checkout session. |
| `cancel_url` | body | `string` | no | Where the customer is redirected after cancelling checkout. |
| `contact` | body | `object` | no | Contact information for the checkout session. |
| `line_items[]` | body | `array<object>` | yes | Line items to include in the checkout session. |
| `order_id` | body | `string` | yes | Your internal order ID for the checkout session. |
| `success_url` | body | `string` | no | Where the customer is redirected after a successful payment. |
| `template_id` | body | `number` | yes | Template ID for the checkout session. |
| `type` | body | `string` | yes | Checkout type, such as invoice. |
| `webhook_url` | body | `string` | no | Webhook URL for checkout updates. |
