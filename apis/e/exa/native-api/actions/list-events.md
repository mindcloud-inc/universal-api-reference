# List Events with Exa

Retrieves events from Exa.

## Endpoint

- **Method:** `GET`
- **Path:** `/websets/v0/events`
- **Base URL:** `https://api.exa.ai`
- **Official documentation:** [List Events](https://exa.ai/docs/websets/api/events/list-all-events)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `types[]` | query | `array<string>` | no | Optional event types to include in the result set. Send multiple values as a array. |
| `createdBefore` | query | `date` | no | Return events created before or at this ISO 8601 timestamp. |
| `createdAfter` | query | `date` | no | Return events created after or at this ISO 8601 timestamp. |
