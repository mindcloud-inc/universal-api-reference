# xAI Video Edit with CometAPI

Creates an xAI video edit in CometAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/grok/v1/videos/edits`
- **Base URL:** `https://api.cometapi.com`
- **Official documentation:** [xAI Video Edit](https://apidoc.cometapi.com/api/video/xai/video-edit)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | yes | Edit prompt. |
| `video` | body | `string` | yes | Video input. |
