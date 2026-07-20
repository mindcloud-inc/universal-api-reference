# Subscribe to Storyboards with Vocal Video

Creates a storyboard webhook subscription in Vocal Video.

## Endpoint

- **Method:** `POST`
- **Path:** `/storyboards/subscribe`
- **Base URL:** `https://vocalvideo.com/api/v1`
- **Official documentation:** [Subscribe to Storyboards](https://help.vocalvideo.com/article/23-using-the-subscription-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `zap[url]` | body | `string` | yes | Public webhook URL to notify when a new storyboard is published. |
