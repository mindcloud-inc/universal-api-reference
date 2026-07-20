# List Purchase Orders with Fiddle

Retrieves purchase order records from Fiddle.

## Endpoint

- **Method:** `GET`
- **Path:** `/purchase-orders`
- **Base URL:** `https://fiddle.io/rest/api/v2`
- **Official documentation:** [List Purchase Orders](https://fiddle.io/rest/api/v2/docs/)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `supplierId` | query | `string` | no | Supplier ID filter |
| `status` | query | `string` | no | Status filter |
