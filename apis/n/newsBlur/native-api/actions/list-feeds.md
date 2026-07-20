# List Feeds with NewsBlur

Retrieves subscribed feeds from NewsBlur.

## Endpoint

- **Method:** `GET`
- **Path:** `/reader/feeds`
- **Base URL:** `https://www.newsblur.com`
- **Official documentation:** [List Feeds](https://newsblur.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include_favicons` | query | `boolean` | no | Include favicons inline in the feeds response. |
| `flat` | query | `boolean` | no | Return a flat folder structure instead of nested folders. |
| `update_counts` | query | `boolean` | no | Force recalculation of unread counts on all feeds. This can slow the request. |
