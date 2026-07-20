# Create Vendor with SOS Inventory

Creates a vendor in SOS Inventory.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/vendor`
- **Base URL:** `https://api.sosinventory.com`
- **Official documentation:** [Create Vendor](https://developer.sosinventory.com/apidoc/Vendor)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name by which you look up this vendor. |
| `email` | body | `string` | no | Vendor email address. |
| `phone` | body | `string` | no | Vendor phone number. |
| `companyName` | body | `string` | no | Company name for this vendor. |
| `notes` | body | `string` | no | Internal notes about this vendor. |
