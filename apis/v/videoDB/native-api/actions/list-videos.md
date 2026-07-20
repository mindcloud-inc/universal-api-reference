# List Videos with VideoDB

Retrieves videos from VideoDB.

## Endpoint

- **Method:** `GET`
- **Path:** `/video/`
- **Base URL:** `https://api.videodb.io`
- **Official documentation:** [List Videos](https://docs.videodb.io/api-reference/videos/list_videos)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection_id` | query | `string` | no | Collection to scope the video list. Defaults to the built-in default collection. |
