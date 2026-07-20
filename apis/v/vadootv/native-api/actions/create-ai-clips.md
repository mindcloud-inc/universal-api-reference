# Create AI clips with Vadootv

Creates an AI clips job in Vadootv.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/create_ai_clips`
- **Base URL:** `https://aiapi.vadoo.tv`
- **Official documentation:** [Create AI clips](https://docs.vadoo.tv/docs/guide/create-ai-clips)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `video_url` | body | `string` | yes | URL of the source long-form video. |
| `num_highlights` | body | `number` | no | Number of viral clips to extract. |
| `aspect_ratio` | body | `list<string>` | no | Target aspect ratio for generated clips. Accepted values: `16:9`, `1:1`, `9:16`. |
| `return_coordinates_only` | body | `boolean` | no | Return bounding box coordinates without rendering the video. |
