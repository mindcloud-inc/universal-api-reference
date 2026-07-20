# List Comment Replies with Vimeo

Retrieves replies to a Vimeo video comment.

## Endpoint

- **Method:** `GET`
- **Path:** `/videos/:video_id/comments/:comment_id/replies`
- **Base URL:** `https://api.vimeo.com`
- **Official documentation:** [List Comment Replies](https://developer.vimeo.com/api/reference/videos#get_comment_replies)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `video_id` | path | `number` | yes | The ID of the video. |
| `comment_id` | path | `number` | yes | The ID of the comment. |
