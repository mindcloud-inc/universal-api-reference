# Get Project Kanban with Easy Projects

Retrieves the kanban board for an Easy Projects project.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/projects/:id/kanban`
- **Base URL:** `https://api.go.easyprojects.net/api/`
- **Official documentation:** [Get Project Kanban](https://api.go.easyprojects.net/api/v1)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Birdview project ID. |
