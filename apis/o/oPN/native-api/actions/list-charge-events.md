# List Charge Events with OPN

Retrieves a list of events for a charge from OPN.

## Endpoint

- **Method:** `GET`
- **Path:** `/charges/:id/events`
- **Base URL:** `https://api.omise.co`
- **Official documentation:** [List Charge Events](https://docs.omise.co/events-api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The charge ID whose events to list. |
