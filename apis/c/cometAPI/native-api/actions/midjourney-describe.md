# Midjourney Describe with CometAPI

Creates a Midjourney prompt from an image in CometAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/mj/submit/describe`
- **Base URL:** `https://api.cometapi.com`
- **Official documentation:** [Midjourney Describe](https://apidoc.cometapi.com/api/image/midjourney/describe)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `base64` | body | `string` | yes | Base64 image input. |
| `link` | body | `string` | yes | Image link input. |
