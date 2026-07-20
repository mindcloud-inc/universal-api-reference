# Update Product with Big Cartel

Updates an existing product in Big Cartel.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/accounts/[:account-id]/products/[:product-id]`
- **Base URL:** `https://api.bigcartel.com`
- **Official documentation:** [Update Product](https://developers.bigcartel.com/api/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account-id` | path | `number` | yes | The Big Cartel account ID. |
| `product-id` | path | `number` | yes | — |
| `id` | body | `number` | yes | — |
