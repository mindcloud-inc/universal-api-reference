# Update Order Expiration with Goody

Updates an order's expiration in Goody.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/orders/:id/update_expiration`
- **Base URL:** `https://api.ongoody.com`
- **Official documentation:** [Update Order Expiration](https://developer.ongoody.com/api-reference/orders/update-expiration-for-an-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `expiration` | body | `date` | no | New expiration date in ISO 8601 format |
