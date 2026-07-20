# List Project Tasks with Trackabi

Retrieves tasks for a project from Trackabi.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/projects/:projectId/tasks`
- **Base URL:** `https://api.trackabi.com`
- **Official documentation:** [List Project Tasks](https://trackabi.com/help/api-docs)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `number` | yes | The unique ID of the project. |
