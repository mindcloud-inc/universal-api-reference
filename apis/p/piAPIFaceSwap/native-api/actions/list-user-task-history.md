# List User Task History with PiAPI/FaceSwap

Retrieves user task history from PiAPI/FaceSwap.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/open/tasks/histories`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [List User Task History](https://piapi.ai/docs/piapi-user-history-query)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | History page number, starting from 1. |
| `page_size` | query | `number` | no | Number of history records per page, max 100. |
| `model` | query | `string` | no | Optional PiAPI model filter such as image_toolkit or video_toolkit. |
| `start_time` | query | `number` | no | Unix timestamp in seconds for the earliest history entry to include. |
| `end_time` | query | `number` | no | Unix timestamp in seconds for the latest history entry to include. |
