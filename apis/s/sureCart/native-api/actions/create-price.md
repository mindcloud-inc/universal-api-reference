# Create Price with SureCart

## Endpoint

- **Method:** `POST`
- **Path:** `v1/prices`
- **Base URL:** `https://api.surecart.com`
- **Official documentation:** [Create Price](https://developer.surecart.com/api-reference/prices/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `price.product_id` | body | `string` | yes | The product ID this price belongs to. |
| `price.amount` | body | `number` | yes | The amount in cents to charge for this price. |
| `price.currency` | body | `string` | yes | Three-letter ISO currency code in lowercase. |
| `price.name` | body | `string` | no | The display name for this price. |
