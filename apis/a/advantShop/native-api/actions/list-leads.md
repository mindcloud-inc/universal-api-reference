# List Leads with AdvantShop

Retrieves leads from AdvantShop.

## Endpoint

- **Method:** `POST`
- **Path:** `/leads/getlist`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [List Leads](https://www.advantshop.net/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | body | `number` | no | Page number. AdvantShop defaults to 1. |
| `itemsPerPage` | body | `number` | no | Number of leads per page. AdvantShop defaults to 100. |
