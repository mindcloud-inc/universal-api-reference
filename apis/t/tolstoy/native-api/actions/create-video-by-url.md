# Create Video by URL with Tolstoy

Creates a new video in Tolstoy from a URL.

## Endpoint

- **Method:** `POST`
- **Path:** `/videos/video`
- **Base URL:** `https://api.gotolstoy.com`
- **Official documentation:** [Create Video by URL](https://developers.gotolstoy.com/api-reference/create-video-by-url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `video.videoUrl` | body | `string` | yes | Hosted video URL |
| `video.name` | body | `string` | no | Optional video name |
| `video.posterUrl` | body | `string` | no | Optional poster image URL |
| `video.gifUrl` | body | `string` | no | Optional animated GIF URL |
