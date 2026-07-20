# Get Project Attachments with Easy Projects

Retrieves attachments from a specific Easy Projects project.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/projects/:id/attachments`
- **Base URL:** `https://api.go.easyprojects.net/api/`
- **Official documentation:** [Get Project Attachments](https://api.go.easyprojects.net/api/v1)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Birdview project ID. |
