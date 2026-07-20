# Kling Text To Audio with CometAPI

Creates audio from text with Kling in CometAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/kling/v1/audio/text-to-audio`
- **Base URL:** `https://api.cometapi.com`
- **Official documentation:** [Kling Text To Audio](https://apidoc.cometapi.com/api/video/kling/text-to-audio)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `duration` | body | `string` | yes | Audio duration. |
| `prompt` | body | `string` | yes | Text to audio prompt. |
