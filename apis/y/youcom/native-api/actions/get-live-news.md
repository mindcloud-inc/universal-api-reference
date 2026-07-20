# Get Live News with You.com

Retrieves live news results from You.com.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.ydc-index.io/livenews`
- **Base URL:** `https://api.you.com`
- **Official documentation:** [Get Live News](https://docs.you.com/custom-solutions/live-news/live-news)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | News search query. |
| `count` | query | `number` | no | Maximum number of news results. |
| `page_num` | query | `number` | no | Pagination page number. |
| `recency` | query | `string` | no | Recency filter. |
