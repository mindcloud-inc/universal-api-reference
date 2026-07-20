# Mark Feeds As Read with NewsBlur

Marks feeds as read in NewsBlur.

## Endpoint

- **Method:** `POST`
- **Path:** `/reader/mark_feed_as_read`
- **Base URL:** `https://www.newsblur.com`
- **Official documentation:** [Mark Feeds As Read](https://newsblur.com/api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `feed_id` | body | `number` | yes | Feed ID to mark as read. NewsBlur supports repeating feed_id for multiple feeds. |
| `cutoff_timestamp` | body | `number` | no | Timestamp cutoff for older or newer stories. |
| `direction` | body | `string` | no | Whether stories older or newer than the cutoff should be marked as read. Accepted values: `0`, `1`. |
