# Get Item Receipts with ServiceTitan

## Endpoint

- **Method:** `GET`
- **Path:** `inventory/v2/tenant/{tenant}/receipts`
- **Base URL:** `https://{baseUrl}/`

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modifiedOnOrAfter` | query | `string` | no | Return items modified on or after certain date/time (in UTC) |
| `modifiedBefore` | query | `string` | no | Return items modified before certain date/time (in UTC) |
| `ids` | query | `string` | no | Send multiple values as a array. |
| `sort` | query | `list` | no | — |
