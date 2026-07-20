# List Sales with Gumroad

Retrieves sales from Gumroad.

## Endpoint

- **Method:** `GET`
- **Path:** `/sales`
- **Base URL:** `https://api.gumroad.com/v2`
- **Official documentation:** [List Sales](https://gumroad.com/api#get-/sales)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `after` | query | `date` | no | Only return sales after this date (YYYY-MM-DD). |
| `before` | query | `date` | no | Only return sales before this date (YYYY-MM-DD). |
| `product_id` | query | `string` | no | Filter sales by this product. |
| `email` | query | `string` | no | Filter sales by this email. |
| `order_id` | query | `number` | no | Filter sales by this order ID. |
