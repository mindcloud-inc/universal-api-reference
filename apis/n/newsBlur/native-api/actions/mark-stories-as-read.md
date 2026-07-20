# Mark Stories As Read with NewsBlur

Marks stories as read in NewsBlur.

## Endpoint

- **Method:** `POST`
- **Path:** `/reader/mark_story_hashes_as_read`
- **Base URL:** `https://www.newsblur.com`
- **Official documentation:** [Mark Stories As Read](https://newsblur.com/api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `story_hash` | body | `string` | yes | Story hash to mark as read. NewsBlur supports repeating story_hash for multiple stories. |
