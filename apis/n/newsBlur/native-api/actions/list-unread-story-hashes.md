# List Unread Story Hashes with NewsBlur

Retrieves unread story hashes from NewsBlur.

## Endpoint

- **Method:** `GET`
- **Path:** `/reader/unread_story_hashes`
- **Base URL:** `https://www.newsblur.com`
- **Official documentation:** [List Unread Story Hashes](https://newsblur.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `feed_id` | query | `number` | no | Feed ID to check. NewsBlur supports repeating feed_id for multiple feeds. |
| `include_timestamps` | query | `boolean` | no | Include timestamps for story dates. |
