# List Builds with SOS Inventory

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/build`
- **Base URL:** `https://api.sosinventory.com`
- **Official documentation:** [List Builds](https://developer.sosinventory.com/apidoc/Build)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | Match build number, ID, comment, location, or output item name. |
| `archived` | query | `list<string>` | no | Accepted values: `no`, `yes`. |
| `from` | query | `date` | no | — |
| `to` | query | `date` | no | — |
| `location` | query | `list<string>` | no | — |
| `createdsince` | query | `date` | no | — |
| `updatedsince` | query | `date` | no | — |
| `summary` | query | `string` | no | Any supplied value returns summary fields only. Leave empty for complete records. |
