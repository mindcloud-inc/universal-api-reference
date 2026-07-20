# Calculate Product Price with AdvantShop

Calculates a product price in AdvantShop.

## Endpoint

- **Method:** `POST`
- **Path:** `/products/{id}/price`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Calculate Product Price](https://www.advantshop.net/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Product identifier from AdvantShop. |
| `offerId` | body | `number` | no | Product offer identifier for price calculation. |
| `amount` | body | `number` | no | Product quantity for price calculation. |
