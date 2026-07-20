# Cast Vote with OneAll

Casts a LoudVoice vote in OneAll.

## Endpoint

- **Method:** `PUT`
- **Path:** `/loudvoice/votes/comments/<comment_token>/authors/<author_token>.json`
- **Base URL:** `https://mindcloudco.api.oneall.com`
- **Official documentation:** [Cast Vote](https://docs.oneall.com/api/resources/loudvoice/votes/cast/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `author_token` | path | `string` | yes | The OneAll author token. |
| `comment_token` | path | `string` | yes | The OneAll comment token. |
