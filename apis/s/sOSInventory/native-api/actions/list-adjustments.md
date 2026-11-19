# List Adjustments with SOS Inventory

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/adjustment`
- **Base URL:** `https://api.sosinventory.com`
- **Official documentation:** [List Adjustments](https://developer.sosinventory.com/apidoc/Adjustment)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | Match adjustment number, ID, comment, or location. |
| `status` | query | `list<string>` | no | Accepted values: `closed`, `open`. |
| `archived` | query | `list<string>` | no | Accepted values: `no`, `yes`. |
| `from` | query | `date` | no | — |
| `to` | query | `date` | no | — |
| `location` | query | `list<string>` | no | — |
| `createdsince` | query | `date` | no | — |
| `updatedsince` | query | `date` | no | — |
| `summary` | query | `string` | no | Any supplied value returns summary fields only. Leave empty for complete records. |
