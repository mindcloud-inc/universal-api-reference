# List Returns with SOS Inventory

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/return`
- **Base URL:** `https://api.sosinventory.com`
- **Official documentation:** [List Returns](https://developer.sosinventory.com/apidoc/Return)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | Match return number, comment, or customer name. |
| `archived` | query | `list<string>` | no | Accepted values: `no`, `yes`. |
| `from` | query | `date` | no | — |
| `to` | query | `date` | no | — |
| `location` | query | `list<string>` | no | — |
| `createdsince` | query | `date` | no | — |
| `updatedsince` | query | `date` | no | — |
| `summary` | query | `string` | no | Any supplied value returns summary fields only. Leave empty for complete records. |
