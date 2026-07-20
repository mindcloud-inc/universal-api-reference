# List Incident Events with FireHydrant

Retrieves incident events from FireHydrant.

## Endpoint

- **Method:** `GET`
- **Path:** `/incidents/:incident_id/events`
- **Base URL:** `https://api.firehydrant.io/v1`
- **Official documentation:** [List Incident Events](https://docs.firehydrant.com/reference/list_incident_events)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `incident_id` | path | `string` | yes | The FireHydrant incident ID. |
| `types` | query | `string` | no | Filter event types. |
