# Update Category with AdvantShop

Updates an existing category in AdvantShop.

## Endpoint

- **Method:** `POST`
- **Path:** `/categories/{id}`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Update Category](https://www.advantshop.net/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Category identifier from AdvantShop. |
| `Name` | body | `string` | no | Updated category name. |
