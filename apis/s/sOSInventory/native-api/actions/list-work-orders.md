# List Work Orders with SOS Inventory

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/workorder`
- **Base URL:** `https://api.sosinventory.com`
- **Official documentation:** [List Work Orders](https://developer.sosinventory.com/apidoc/WorkOrder)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | Match work order number, customer, or comments. |
| `status` | query | `list<string>` | no | Accepted values: `closed`, `open`. |
| `archived` | query | `list<string>` | no | Accepted values: `no`, `yes`. |
| `from` | query | `date` | no | — |
| `to` | query | `date` | no | — |
| `createdsince` | query | `date` | no | — |
| `updatedsince` | query | `date` | no | — |
| `summary` | query | `string` | no | Any supplied value returns summary fields only. Leave empty for complete records. |
