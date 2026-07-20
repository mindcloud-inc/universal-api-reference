# Get Video Result with xAI

Retrieves a video result from the xAI API.

## Endpoint

- **Method:** `GET`
- **Path:** `/videos/:request_id`
- **Base URL:** `https://api.x.ai/v1`
- **Official documentation:** [Get Video Result](https://docs.x.ai/developers/rest-api-reference/inference/videos#get-video-result)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request_id` | path | `string` | no | Deferred video request ID returned by a video generation or edit request. |
