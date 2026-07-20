# List Product Stocks with AdvantShop

Retrieves product stock levels from AdvantShop.

## Endpoint

- **Method:** `GET`
- **Path:** `/products/{id}/stocks`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [List Product Stocks](https://www.advantshop.net/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Product identifier from AdvantShop. |
| `offerId` | query | `number` | no | Optional product offer identifier for stock lookup. |
