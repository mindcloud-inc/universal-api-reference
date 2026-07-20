# Save Story with NewsBlur

Saves a story in NewsBlur.

## Endpoint

- **Method:** `POST`
- **Path:** `/reader/mark_story_hash_as_starred`
- **Base URL:** `https://www.newsblur.com`
- **Official documentation:** [Save Story](https://newsblur.com/api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `story_hash` | body | `string` | yes | Story hash to save. |
| `user_tags[]` | body | `array<string>` | no | Tags to apply to the saved story. Send multiple values as a array. |
| `highlights[]` | body | `array<string>` | no | Strings to highlight on the saved story. Send multiple values as a array. |
