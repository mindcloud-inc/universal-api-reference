# List Shipments with Rye

Retrieves shipments from Rye.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/shipments`
- **Base URL:** `https://staging.api.rye.com`
- **Official documentation:** [List Shipments](https://rye.com/docs/api-v2/introduction)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids[]` | query | `array<string>` | no | Filter by shipment ids. Send multiple values as a array. |
| `status[]` | query | `array<string>` | no | Filter by shipment statuses. Send multiple values as a array. |
