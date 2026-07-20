# Update Shipment with SOS Inventory

Updates an existing shipment in SOS Inventory.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v2/shipment/:id`
- **Base URL:** `https://api.sosinventory.com`
- **Official documentation:** [Update Shipment](https://developer.sosinventory.com/apidoc/Shipment)

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
| `customer.name` | body | `string` | yes |
| `location.name` | body | `string` | yes |
| `comment` | body | `string` | no |
| `lines[].item.name` | body | `string` | yes |
| `lines[].quantity` | body | `number` | yes |
