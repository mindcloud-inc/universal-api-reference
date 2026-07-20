# Update Video with VideoDB

Updates an existing video in VideoDB.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/video/:video_id`
- **Base URL:** `https://api.videodb.io`
- **Official documentation:** [Update Video](https://docs.videodb.io/api-reference/videos/update_video)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `video_id` | path | `string` | yes | Video ID |
| `name` | body | `string` | no | Updated video name |
