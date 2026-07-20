# Update Brand Video Tags with Orshot

## Endpoint

- **Method:** `PATCH`
- **Path:** `/brand-assets/videos/update/:id`
- **Base URL:** `https://api.orshot.com/v1`
- **Official documentation:** [Update Brand Video Tags](https://orshot.com/docs/api-reference/brand-videos-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The brand video ID. |
| `tags[]` | body | `array<string>` | yes | The tags to set on the video, replacing existing tags. |
