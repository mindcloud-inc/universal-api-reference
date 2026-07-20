# List Events with Optimizely

Retrieves a list of events from Optimizely.

## Endpoint

- **Method:** `GET`
- **Path:** `/events`
- **Base URL:** `https://api.optimizely.com/v2`
- **Official documentation:** [List Events](https://docs.developers.optimizely.com/web-experimentation/reference/list_events)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | query | `string` | yes | Filter events to one project. |
