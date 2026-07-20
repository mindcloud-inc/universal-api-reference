# Create Order with Tremendous

Creates a new order in Tremendous.

## Endpoint

- **Method:** `POST`
- **Path:** `/orders`
- **Base URL:** `https://testflight.tremendous.com/api/v2`
- **Official documentation:** [Create Order](https://developers.tremendous.com/reference/create-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `external_id` | body | `string` | no | Client-side idempotency key for the order |
| `payment` | body | `object` | yes | Payment object containing the funding source to charge |
| `payment.funding_source_id` | body | `string` | yes | Tremendous funding source ID used to pay for the order |
| `reward` | body | `object` | yes | Reward object describing value, recipient, and delivery |
| `reward.campaign_id` | body | `string` | no | Campaign ID that controls the reward products and presentation |
| `reward.delivery` | body | `object` | no | Reward delivery object |
| `reward.delivery.method` | body | `string` | yes | Delivery method for the reward |
| `reward.products[]` | body | `array<string>` | no | List of Tremendous product IDs available to the recipient |
| `reward.recipient` | body | `object` | no | Reward recipient object |
| `reward.recipient.email` | body | `string` | yes | Recipient email address |
| `reward.recipient.name` | body | `string` | yes | Recipient name |
| `reward.value` | body | `object` | no | Reward value object |
| `reward.value.currency_code` | body | `string` | no | ISO currency code for the reward value |
| `reward.value.denomination` | body | `number` | yes | Monetary amount of the reward |
