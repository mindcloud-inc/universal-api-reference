# Get Project Tasks with Easy Projects

Retrieves tasks from a specific Easy Projects project.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/projects/:id/tasks`
- **Base URL:** `https://api.go.easyprojects.net/api/`
- **Official documentation:** [Get Project Tasks](https://api.go.easyprojects.net/api/v1)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Birdview project ID. |
