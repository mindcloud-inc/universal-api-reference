# List Customers with AdvantShop

Retrieves customers from AdvantShop.

## Endpoint

- **Method:** `GET`
- **Path:** `/customers`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [List Customers](https://www.advantshop.net/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number. AdvantShop defaults to 1. |
| `itemsPerPage` | query | `number` | no | Number of customers per page. AdvantShop defaults to 100. |
