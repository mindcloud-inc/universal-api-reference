# Calculate Order Batch Price with Goody

Calculates an order batch price in Goody.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/order_batches/price`
- **Base URL:** `https://api.ongoody.com`
- **Official documentation:** [Calculate Order Batch Price](https://developer.ongoody.com/api-reference/order-batches/calculate-the-price-for-an-order-batch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `recipients[]` | body | `array<object>` | yes | — |
| `cart` | body | `object` | yes | — |
| `send_method` | body | `string` | yes | The method for sending a order batch. `email_and_link` sends a gift email to the recipient (specify `email` for each recipient). `link_multiple_custom_list` generates a gift link without an automatic email. `direct_send` ships the product directly to the recipient (specify `mailing_address` for each recipient). For more information, see [Send Methods](/introduction/send-methods). |
