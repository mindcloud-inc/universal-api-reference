# Upload Brand Video with Orshot

## Endpoint

- **Method:** `POST`
- **Path:** `/brand-assets/videos/add`
- **Base URL:** `https://api.orshot.com/v1`
- **Official documentation:** [Upload Brand Video](https://orshot.com/docs/api-reference/brand-videos-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `string` | yes | The video file content or source. |
| `filename` | body | `string` | no | The uploaded video filename. |
| `tags[]` | body | `array<string>` | no | Tags to associate with the video. |
