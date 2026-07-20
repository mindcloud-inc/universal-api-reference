# Get Project Members with Easy Projects

Retrieves members of a specific Easy Projects project.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/projects/:id/members`
- **Base URL:** `https://api.go.easyprojects.net/api/`
- **Official documentation:** [Get Project Members](https://api.go.easyprojects.net/api/v1)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Birdview project ID. |
