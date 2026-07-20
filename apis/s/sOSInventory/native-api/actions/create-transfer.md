# Create Transfer with SOS Inventory

Creates a transfer in SOS Inventory.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/transfer`
- **Base URL:** `https://api.sosinventory.com`
- **Official documentation:** [Create Transfer](https://developer.sosinventory.com/apidoc/Transfer)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `number` | body | `string` | no |
| `date` | body | `string` | yes |
| `fromLocation.name` | body | `string` | yes |
| `toLocation.name` | body | `string` | yes |
| `comment` | body | `string` | no |
| `lines[].item.name` | body | `string` | yes |
| `lines[].quantity` | body | `number` | yes |
