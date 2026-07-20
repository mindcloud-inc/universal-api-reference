# Create Customer with SOS Inventory

Creates a customer in SOS Inventory.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/customer`
- **Base URL:** `https://api.sosinventory.com`
- **Official documentation:** [Create Customer](https://developer.sosinventory.com/apidoc/Customer)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name by which you look up this customer. |
| `email` | body | `string` | no | Customer email address. |
| `phone` | body | `string` | no | Customer phone number. |
| `companyName` | body | `string` | no | Company name for this customer. |
| `notes` | body | `string` | no | Internal notes about the customer. |
