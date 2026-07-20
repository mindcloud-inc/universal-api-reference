# Midjourney Imagine with CometAPI

Creates a Midjourney imagine task in CometAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/mj/submit/imagine`
- **Base URL:** `https://api.cometapi.com`
- **Official documentation:** [Midjourney Imagine](https://apidoc.cometapi.com/api/image/midjourney/imagine)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | yes | Midjourney prompt. |
