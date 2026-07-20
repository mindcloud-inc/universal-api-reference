# Delete Location with NetSuite - Basic

Deletes an existing location from NetSuite.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/record/v1/location/:id`
- **Base URL:** `https://{accountDomain}.suitetalk.api.netsuite.com/services/rest`
- **Official documentation:** [Delete Location](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/location)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | no | Internal NetSuite record ID. |
