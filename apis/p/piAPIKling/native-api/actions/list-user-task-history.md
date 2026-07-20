# List User Task History with PiAPI/Kling

## Endpoint

- **Method:** `GET`
- **Path:** `/api/open/tasks/histories`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [List User Task History](https://piapi.ai/docs/piapi-user-history-query)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number. PiAPI starts paging at 1. |
| `page_size` | query | `number` | no | Number of history records to return. PiAPI defaults to 10 and allows up to 100. |
| `model` | query | `string` | no | Filter history to one PiAPI model. Use kling for Kling tasks. |
| `start_time` | query | `number` | no | Unix timestamp in seconds. Return tasks created at or after this time. |
| `end_time` | query | `number` | no | Unix timestamp in seconds. Return tasks created at or before this time. |
