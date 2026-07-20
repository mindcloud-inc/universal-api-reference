# Get Inventory with Alto

Retrieves inventory records from your Alto account.

## Endpoint

- **Method:** `GET`
- **Path:** `/inventory`
- **Base URL:** `https://api.alto.zoopladev.co.uk`
- **Official documentation:** [Get Inventory](https://developers.vebraalto.com/api)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | query | `string` | no | Address text to filter inventory results. |
| `category` | query | `string` | no | Inventory category filter. |
| `recordType` | query | `string` | no | Inventory record type filter. |
| `archived` | query | `boolean` | no | Whether to include archived inventory records. |
