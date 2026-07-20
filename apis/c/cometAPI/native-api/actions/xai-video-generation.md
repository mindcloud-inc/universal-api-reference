# xAI Video Generation with CometAPI

Creates an xAI video generation task in CometAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/grok/v1/videos/generations`
- **Base URL:** `https://api.cometapi.com`
- **Official documentation:** [xAI Video Generation](https://apidoc.cometapi.com/api/video/xai/video-generation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | yes | Video generation prompt. |
