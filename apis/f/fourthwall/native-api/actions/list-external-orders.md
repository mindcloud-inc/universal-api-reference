# List External Orders with Fourthwall

Retrieves external orders from Fourthwall with optional filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/open-api/v1.0/external-orders`
- **Base URL:** `https://api.fourthwall.com`
- **Official documentation:** [List External Orders](https://docs.fourthwall.com/api-reference/platform/external-orders/list-external-orders)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `externalSource` | query | `string` | no | Filter external orders by source. |
| `externalOrderId` | query | `string` | no | Filter external orders by external order ID. |
| `status` | query | `string` | no | Filter external orders by status. Send multiple values as a array. |
| `createdAfter` | query | `date` | no | Filter external orders created after this timestamp. |
| `createdBefore` | query | `date` | no | Filter external orders created before this timestamp. |
