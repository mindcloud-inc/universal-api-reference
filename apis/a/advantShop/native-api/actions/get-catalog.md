# Get Catalog with AdvantShop

Retrieves the catalog from AdvantShop.

## Endpoint

- **Method:** `POST`
- **Path:** `/catalog`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Get Catalog](https://www.advantshop.net/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `categoryId` | body | `number` | no | Category ID. AdvantShop requires either categoryId or url for catalog requests. |
| `url` | body | `string` | no | Category URL. AdvantShop requires either categoryId or url for catalog requests. |
