# Search Feed with NewsBlur

Finds a feed in NewsBlur by website or RSS address.

## Endpoint

- **Method:** `GET`
- **Path:** `/rss_feeds/search_feed`
- **Base URL:** `https://www.newsblur.com`
- **Official documentation:** [Search Feed](https://newsblur.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | query | `string` | yes | RSS feed address or website address to search. |
| `offset` | query | `number` | no | Offset for paging through feed search results. |
