# Delete Vote with OneAll

Deletes a LoudVoice vote from OneAll.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/loudvoice/votes/comments/<comment_token>/authors/<author_token>.json`
- **Base URL:** `https://mindcloudco.api.oneall.com`
- **Official documentation:** [Delete Vote](https://docs.oneall.com/api/resources/loudvoice/votes/delete/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `author_token` | path | `string` | yes | The OneAll author token. |
| `comment_token` | path | `string` | yes | The OneAll comment token. |
