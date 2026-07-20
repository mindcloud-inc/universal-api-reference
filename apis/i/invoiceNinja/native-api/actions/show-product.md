# Show Product with Invoice Ninja

## Endpoint

- **Method:** `GET`
- **Path:** `/products/:id`
- **Base URL:** `https://invoicing.co/api/v1`
- **Official documentation:** [Show Product](https://api-docs.invoicing.co/#tag/products/operation/showProduct)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Hashed product ID. |
| `include` | query | `string` | no | Optional related records to include in the response. |
