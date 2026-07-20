# Get Inventory Item with NetSuite - Basic

Retrieves details for the inventory item in NetSuite.

## Endpoint

- **Method:** `GET`
- **Path:** `/record/v1/inventoryItem/:id`
- **Base URL:** `https://{accountDomain}.suitetalk.api.netsuite.com/services/rest`
- **Official documentation:** [Get Inventory Item](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/inventoryItem)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | no | Internal NetSuite record ID. |
