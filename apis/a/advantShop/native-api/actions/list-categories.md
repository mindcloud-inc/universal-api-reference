# List Categories with AdvantShop

Retrieves categories from AdvantShop.

## Endpoint

- **Method:** `GET`
- **Path:** `/categories`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [List Categories](https://www.advantshop.net/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number. AdvantShop defaults to 1. |
| `itemsPerPage` | query | `number` | no | Number of categories per page. AdvantShop defaults to 100 and supports up to 500. |
