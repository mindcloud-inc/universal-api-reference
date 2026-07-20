# Kling Image Generation with CometAPI

Creates a Kling image in CometAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/kling/v1/images/generations`
- **Base URL:** `https://api.cometapi.com`
- **Official documentation:** [Kling Image Generation](https://apidoc.cometapi.com/api/video/kling/image-generation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | yes | Image generation prompt. |
