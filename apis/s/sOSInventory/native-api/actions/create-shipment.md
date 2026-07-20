# Create Shipment with SOS Inventory

Creates a shipment in SOS Inventory.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/shipment`
- **Base URL:** `https://api.sosinventory.com`
- **Official documentation:** [Create Shipment](https://developer.sosinventory.com/apidoc/Shipment)

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
| `customer.name` | body | `string` | yes |
| `location.name` | body | `string` | yes |
| `comment` | body | `string` | no |
| `lines[].item.name` | body | `string` | yes |
| `lines[].quantity` | body | `number` | yes |
