# Get Vote with OneAll

Retrieves a LoudVoice vote from OneAll.

## Endpoint

- **Method:** `GET`
- **Path:** `/loudvoice/votes/comments/<comment_token>/authors/<author_token>.json`
- **Base URL:** `https://mindcloudco.api.oneall.com`
- **Official documentation:** [Get Vote](https://docs.oneall.com/api/resources/loudvoice/votes/read/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `author_token` | path | `string` | yes | The OneAll author token. |
| `comment_token` | path | `string` | yes | The OneAll comment token. |
