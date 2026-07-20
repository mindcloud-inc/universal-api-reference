# Rate Video with YouTube

Sets the authenticated user's rating for a YouTube video.

## Endpoint

- **Method:** `POST`
- **Path:** `/youtube/v3/videos/rate`
- **Base URL:** `https://www.googleapis.com`
- **Official documentation:** [Rate Video](https://developers.google.com/youtube/v3/docs/videos/rate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | YouTube video ID. |
| `rating` | query | `string` | yes | Rating to set for the video. |
| `onBehalfOfContentOwner` | query | `string` | no | Content owner ID when acting on behalf of a CMS user. |
