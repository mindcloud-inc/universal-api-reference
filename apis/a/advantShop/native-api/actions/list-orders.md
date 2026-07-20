# List Orders with AdvantShop

Retrieves orders from AdvantShop.

## Endpoint

- **Method:** `POST`
- **Path:** `/order/getlist`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [List Orders](https://www.advantshop.net/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Page` | body | `number` | no | Page number. AdvantShop defaults to 1. |
| `ItemsPerPage` | body | `number` | no | Number of orders per page. AdvantShop defaults to 100. |
