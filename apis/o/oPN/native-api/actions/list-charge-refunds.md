# List Charge Refunds with OPN

Retrieves a list of refunds for a charge from OPN.

## Endpoint

- **Method:** `GET`
- **Path:** `/charges/:id/refunds`
- **Base URL:** `https://api.omise.co`
- **Official documentation:** [List Charge Refunds](https://docs.omise.co/refunds-api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The charge ID whose refunds to list. |
