# Update Customer with SOS Inventory

Updates an existing customer in SOS Inventory.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v2/customer/:id`
- **Base URL:** `https://api.sosinventory.com`
- **Official documentation:** [Update Customer](https://developer.sosinventory.com/apidoc/Customer)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The SOS customer ID to update. |
| `syncToken` | body | `string` | yes | The current sync token for this customer. |
| `id` | body | `number` | yes | The SOS customer ID inside the request body, which must match the path ID. |
| `name` | body | `string` | yes | The name by which you look up this customer. |
| `email` | body | `string` | no | Customer email address. |
| `phone` | body | `string` | no | Customer phone number. |
| `companyName` | body | `string` | no | Company name for this customer. |
| `notes` | body | `string` | no | Internal notes about the customer. |
