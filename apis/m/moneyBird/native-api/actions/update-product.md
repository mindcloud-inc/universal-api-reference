# Update Product with MoneyBird

Updates an existing product in MoneyBird.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/:administrationId/products/:productId.json`
- **Base URL:** `https://moneybird.com/api/v2`
- **Official documentation:** [Update Product](https://developer.moneybird.com/api/products)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `administrationId` | path | `string` | yes | Moneybird administration ID. |
| `productId` | path | `string` | yes | Moneybird product ID. |
