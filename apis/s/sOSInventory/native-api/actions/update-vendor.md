# Update Vendor with SOS Inventory

Updates an existing vendor in SOS Inventory.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v2/vendor/:id`
- **Base URL:** `https://api.sosinventory.com`
- **Official documentation:** [Update Vendor](https://developer.sosinventory.com/apidoc/Vendor)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The SOS vendor ID to update. |
| `syncToken` | body | `string` | yes | The current sync token for this vendor. |
| `id` | body | `number` | yes | The SOS vendor ID inside the request body, which must match the path ID. |
| `name` | body | `string` | yes | The name by which you look up this vendor. |
| `email` | body | `string` | no | Vendor email address. |
| `phone` | body | `string` | no | Vendor phone number. |
| `companyName` | body | `string` | no | Company name for this vendor. |
| `notes` | body | `string` | no | Internal notes about this vendor. |
