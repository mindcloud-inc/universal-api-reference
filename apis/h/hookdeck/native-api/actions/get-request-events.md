# Get Request Events with Hookdeck

Retrieves events for a request in Hookdeck.

## Endpoint

- **Method:** `GET`
- **Path:** `/requests/:id/events`
- **Base URL:** `https://api.hookdeck.com/2025-07-01`
- **Official documentation:** [Get Request Events](https://hookdeck.com/docs/api/inspect.md#requests)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Hookdeck request ID from the `id` path parameter. |
