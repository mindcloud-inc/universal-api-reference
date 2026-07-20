# List Posts with Curator

Retrieves posts for a feed in Curator.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/feeds/:FEED_ID/posts`
- **Base URL:** `https://api.curator.io`
- **Official documentation:** [List Posts](https://curator.io/docs/api/posts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `FEED_ID` | path | `string` | yes | ID of the feed whose posts should be listed. |
| `limit` | query | `number` | no | Optional page size. |
| `after` | query | `string` | no | Pagination cursor for the next page. |
| `before` | query | `string` | no | Pagination cursor for the previous page. |
| `network_id` | query | `number` | no | Optional network filter. |
| `source_type` | query | `number` | no | Optional source type filter. |
| `status` | query | `string` | no | Optional post status filter. |
