# Get Task Attachments with Easy Projects

Retrieves attachments from an Easy Projects task.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/tasks/:id/attachments`
- **Base URL:** `https://api.go.easyprojects.net/api/`
- **Official documentation:** [Get Task Attachments](https://api.go.easyprojects.net/api/v1)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Birdview task ID. |
