# Mark Story As Unread with NewsBlur

Marks stories as unread in NewsBlur.

## Endpoint

- **Method:** `POST`
- **Path:** `/reader/mark_story_hash_as_unread`
- **Base URL:** `https://www.newsblur.com`
- **Official documentation:** [Mark Story As Unread](https://newsblur.com/api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `story_hash` | body | `string` | yes | Story hash to mark as unread. |
