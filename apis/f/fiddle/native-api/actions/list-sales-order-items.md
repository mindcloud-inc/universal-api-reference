# List Sales Order Items with Fiddle

Retrieves sales order items from Fiddle.

## Endpoint

- **Method:** `GET`
- **Path:** `/sales-order-items`
- **Base URL:** `https://fiddle.io/rest/api/v2`
- **Official documentation:** [List Sales Order Items](https://fiddle.io/rest/api/v2/docs/)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `salesOrderId` | query | `string` | no | Sales order ID filter |
