# Get Video Generation Results with Grok

Retrieves results for a video generation request from Grok.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/videos/:request_id`
- **Base URL:** `https://api.x.ai`
- **Official documentation:** [Get Video Generation Results](https://docs.x.ai/developers/rest-api-reference/inference/videos#get-video-generation-results)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request_id` | path | `string` | yes | Video generation request identifier. |
