# Kling Text To Video with CometAPI

Creates a Kling text-to-video task in CometAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/kling/v1/videos/text2video`
- **Base URL:** `https://api.cometapi.com`
- **Official documentation:** [Kling Text To Video](https://apidoc.cometapi.com/api/video/kling/text-to-video)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | yes | Text to video prompt. |
