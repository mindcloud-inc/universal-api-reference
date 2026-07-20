# List Videos with Twitch

Retrieves video records and metadata from Twitch.

## Endpoint

- **Method:** `GET`
- **Path:** `/videos`
- **Base URL:** `https://api.twitch.tv/helix`
- **Official documentation:** [List Videos](https://dev.twitch.tv/docs/api/reference#get-videos)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | no | An ID that identifies the video to get. Specify this parameter up to 100 times. Send multiple values as a array. |
| `user_id` | query | `string` | no | The ID of the user who owns the video. |
| `game_id` | query | `string` | no | The ID of the game whose videos you want to get. |
| `language` | query | `string` | no | A filter to limit the response to videos in the specified language. |
| `period` | query | `string` | no | A filter that determines the period during which the video was created. |
| `sort` | query | `string` | no | Sort order for the results. Valid values are time, trending, and views. |
| `type` | query | `string` | no | Filter videos by type. Valid values are all, upload, archive, and highlight. |
| `first` | query | `number` | no | Maximum number of videos to return. Minimum 1, maximum 100. |
| `after` | query | `string` | no | Cursor for forward pagination. |
| `before` | query | `string` | no | Cursor for backward pagination. |
