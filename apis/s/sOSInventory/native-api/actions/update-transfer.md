# Update Transfer with SOS Inventory

Updates an existing transfer in SOS Inventory.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v2/transfer/:id`
- **Base URL:** `https://api.sosinventory.com`
- **Official documentation:** [Update Transfer](https://developer.sosinventory.com/apidoc/Transfer)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
| `number` | body | `string` | yes |
| `date` | body | `string` | yes |
| `fromLocation.name` | body | `string` | yes |
| `toLocation.name` | body | `string` | yes |
| `comment` | body | `string` | no |
| `lines[].item.name` | body | `string` | yes |
| `lines[].quantity` | body | `number` | yes |
