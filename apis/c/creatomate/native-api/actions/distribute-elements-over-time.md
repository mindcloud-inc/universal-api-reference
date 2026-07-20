# Distribute Elements Over Time with Creatomate

Creates a render that distributes elements over time.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/renders`
- **Base URL:** `https://api.creatomate.com`
- **Official documentation:** [Distribute Elements Over Time](https://creatomate.com/docs/api/quick-start/distribute-elements-over-time)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `backgroundAudioUrl` | body | `string` | yes | Audio track used as the timeline anchor for the fractional distribution. |
| `mediaUrls[]` | body | `array<string>` | yes | Ordered list of image or video URLs to distribute evenly over the timeline. |
| `mediaType` | body | `string` | no | Whether the distributed media items are images or videos. |
| `loopVideos` | body | `boolean` | no | Whether distributed video elements should loop to fill their fractional duration. |
