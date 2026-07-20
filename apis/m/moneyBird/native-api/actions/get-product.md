# Get Product with MoneyBird

Retrieves a product from MoneyBird.

## Endpoint

- **Method:** `GET`
- **Path:** `/:administrationId/products/:productId.json`
- **Base URL:** `https://moneybird.com/api/v2`
- **Official documentation:** [Get Product](https://developer.moneybird.com/api/products)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `administrationId` | path | `string` | yes | Moneybird administration ID. |
| `productId` | path | `string` | yes | Moneybird product ID. |
