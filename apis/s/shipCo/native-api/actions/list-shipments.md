# List Shipments with Ship&Co

## Endpoint

- **Method:** `GET`
- **Path:** `/shipments`
- **Base URL:** `https://api.shipandco.com/v1`
- **Official documentation:** [List Shipments](https://developer.shipandco.com/en/#shipment)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `carrier` | query | `string` | no | Optional carrier type filter. |
| `scope` | query | `string` | no | Shipment scope: api or all. |
| `state` | query | `string` | no | Shipment state: active, void, or any. |
| `created_after` | query | `date` | no | Only include shipments created after this ISO timestamp. |
| `created_before` | query | `date` | no | Only include shipments created before this ISO timestamp. |
