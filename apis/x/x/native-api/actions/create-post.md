# Create Post with X

## Endpoint

- **Method:** `POST`
- **Path:** `/2/tweets`
- **Base URL:** `https://api.x.com`
- **Official documentation:** [Create Post](https://docs.x.com/x-api/posts/create-post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | no | The text of your post (up to 280 characters). Maximum length: 280. |
| `media.media_ids[]` | body | `array<string>` | no | Array of media IDs (from the Upload Media action) to attach to the post. Max 4 images or 1 video/GIF. |
