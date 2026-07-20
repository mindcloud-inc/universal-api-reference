# Get Video Details with VideoDB

Retrieves video details from VideoDB.

## Endpoint

- **Method:** `GET`
- **Path:** `/video/:video_id`
- **Base URL:** `https://api.videodb.io`
- **Official documentation:** [Get Video Details](https://docs.videodb.io/api-reference/videos/get_video)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection_id` | query | `string` | no | Collection containing the video. Defaults to the built-in default collection. |
| `video_id` | path | `string` | no | Video ID to retrieve. |
