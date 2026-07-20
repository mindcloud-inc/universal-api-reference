# List Changes with Optimizely

Retrieves project change history from the Optimizely API.

## Endpoint

- **Method:** `GET`
- **Path:** `/changes`
- **Base URL:** `https://api.optimizely.com/v2`
- **Official documentation:** [List Changes](https://docs.developers.optimizely.com/web-experimentation/reference/list_change_history)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | query | `string` | yes | The project id to list change history for. |
