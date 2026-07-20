# Get Feed Stories with NewsBlur

Retrieves stories from a feed in NewsBlur.

## Endpoint

- **Method:** `GET`
- **Path:** `/reader/feed/:id`
- **Base URL:** `https://www.newsblur.com`
- **Official documentation:** [Get Feed Stories](https://newsblur.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Feed ID to retrieve stories from. |
| `order` | query | `string` | no | Story order: newest or oldest. Accepted values: `0`, `1`. |
| `read_filter` | query | `string` | no | Show all stories or only unread stories. Accepted values: `0`, `1`. |
| `date_filter_start` | query | `date` | no | Only include stories published on or after this date in YYYY-MM-DD format. |
| `date_filter_end` | query | `date` | no | Only include stories published on or before this date in YYYY-MM-DD format. |
| `include_hidden` | query | `boolean` | no | Include hidden stories. |
| `include_story_content` | query | `boolean` | no | Include story content in the response. |
| `query` | query | `string` | no | Search keyword or phrase in the feed. NewsBlur notes feed search is premium-only. |
