# Create Post with Late

## Endpoint

- **Method:** `POST`
- **Path:** `/posts`
- **Base URL:** `https://zernio.com/api/v1`
- **Official documentation:** [Create Post](https://docs.zernio.com/posts/create-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | no | — |
| `content` | body | `string` | no | Post caption/text for the draft seed post. |
| `isDraft` | body | `boolean` | no | Hidden default to force deterministic draft creation for verification setup. |
| `scheduledFor` | body | `string` | no | — |
| `publishNow` | body | `boolean` | no | — |
| `timezone` | body | `string` | no | — |
| `queuedFromProfile` | body | `string` | no | — |
| `queueId` | body | `string` | no | — |
| `mediaItems[]` | body | `array<object>` | no | — |
| `platforms[]` | body | `array<object>` | no | — |
| `tags[]` | body | `array<string>` | no | — |
| `hashtags[]` | body | `array<string>` | no | — |
| `mentions[]` | body | `array<string>` | no | — |
| `crosspostingEnabled` | body | `boolean` | no | — |
| `metadata` | body | `object` | no | — |
| `tiktokSettings` | body | `object` | no | — |
| `recycling` | body | `object` | no | — |
