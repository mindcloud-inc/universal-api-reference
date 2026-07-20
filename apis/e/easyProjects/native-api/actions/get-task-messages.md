# Get Task Messages with Easy Projects

Retrieves messages from an Easy Projects task.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/tasks/:id/messages`
- **Base URL:** `https://api.go.easyprojects.net/api/`
- **Official documentation:** [Get Task Messages](https://api.go.easyprojects.net/api/v1)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Birdview task ID. |
