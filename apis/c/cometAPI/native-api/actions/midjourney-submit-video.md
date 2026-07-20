# Midjourney Submit Video with CometAPI

Creates a Midjourney video task in CometAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/mj/submit/video`
- **Base URL:** `https://api.cometapi.com`
- **Official documentation:** [Midjourney Submit Video](https://apidoc.cometapi.com/api/image/midjourney/submit-video)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `string` | yes | Image input. |
| `motion` | body | `string` | yes | Video motion preset. |
