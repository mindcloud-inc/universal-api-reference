# List Webhooks with Optimizely

Retrieves webhooks for a project in Optimizely.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{projectId}/webhooks`
- **Base URL:** `https://api.optimizely.com/v2`
- **Official documentation:** [List Webhooks](https://docs.developers.optimizely.com/web-experimentation/reference/list_webhooks)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | The project id to list webhooks for. |
