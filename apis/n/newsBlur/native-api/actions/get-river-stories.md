# Get River Stories with NewsBlur

Retrieves stories from multiple feeds in NewsBlur.

## Endpoint

- **Method:** `GET`
- **Path:** `/reader/river_stories`
- **Base URL:** `https://www.newsblur.com`
- **Official documentation:** [Get River Stories](https://newsblur.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `feeds` | query | `number` | yes | Feed ID to include in the River of News. NewsBlur supports repeating feeds for multiple feeds. |
| `order` | query | `string` | no | Story order: newest or oldest. Accepted values: `0`, `1`. |
| `read_filter` | query | `string` | no | Show all stories or only unread stories. Accepted values: `0`, `1`. |
| `date_filter_start` | query | `date` | no | Only include stories published on or after this date in YYYY-MM-DD format. |
| `date_filter_end` | query | `date` | no | Only include stories published on or before this date in YYYY-MM-DD format. |
| `include_hidden` | query | `boolean` | no | Include hidden stories. |
| `query` | query | `string` | no | Search keyword or phrase in the folder. NewsBlur notes feed search is premium-only. |
| `infrequent` | query | `string` | no | Show only stories from infrequently published sites, using a stories-per-month value or false. |
