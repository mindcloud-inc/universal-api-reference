# List Checkout Intent Shipments with Rye

Retrieves shipments for a checkout intent in Rye.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/checkout-intents/{id}/shipments`
- **Base URL:** `https://staging.api.rye.com`
- **Official documentation:** [List Checkout Intent Shipments](https://rye.com/docs/api-v2/introduction)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The checkout intent id. |
