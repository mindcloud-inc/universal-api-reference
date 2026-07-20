# Unsave Story with NewsBlur

Removes a saved story from NewsBlur.

## Endpoint

- **Method:** `POST`
- **Path:** `/reader/mark_story_hash_as_unstarred`
- **Base URL:** `https://www.newsblur.com`
- **Official documentation:** [Unsave Story](https://newsblur.com/api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `story_hash` | body | `string` | yes | Story hash to unsave. |
