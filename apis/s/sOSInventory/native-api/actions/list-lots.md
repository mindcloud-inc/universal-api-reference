# List Lots with SOS Inventory

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/lot`
- **Base URL:** `https://api.sosinventory.com`
- **Official documentation:** [List Lots](https://developer.sosinventory.com/apidoc/Lot)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | Match lot number, description, or item name. |
| `status` | query | `list<string>` | no | Accepted values: `expired`, `notexpirednotrecalled`, `recalled`. |
| `archived` | query | `list<string>` | no | Accepted values: `no`, `yes`. |
| `location` | query | `list<string>` | no | Calculate quantity totals for this location. |
| `createdsince` | query | `date` | no | — |
| `updatedsince` | query | `date` | no | — |
