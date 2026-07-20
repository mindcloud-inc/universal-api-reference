# xAI Get Video Result with CometAPI

Retrieves an xAI video result from CometAPI.

## Endpoint

- **Method:** `GET`
- **Path:** `/grok/v1/videos/:request_id`
- **Base URL:** `https://api.cometapi.com`
- **Official documentation:** [xAI Get Video Result](https://apidoc.cometapi.com/api/video/xai/get-video-generation-results)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request_id` | path | `string` | yes | xAI request identifier. |
