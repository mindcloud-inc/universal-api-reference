# Midjourney Submit Editor with CometAPI

Creates a Midjourney editor task in CometAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/mj/submit/edits`
- **Base URL:** `https://api.cometapi.com`
- **Official documentation:** [Midjourney Submit Editor](https://apidoc.cometapi.com/api/image/midjourney/submit-editor)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `string` | yes | Image input. |
| `prompt` | body | `string` | yes | Edit prompt. |
