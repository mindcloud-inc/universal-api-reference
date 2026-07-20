# Search Crawl Or Bulk Job with Diffbot

Searches a Diffbot crawl or bulk job with DQL.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/search/`
- **Base URL:** `https://api.diffbot.com`
- **Official documentation:** [Search Crawl Or Bulk Job](https://docs.diffbot.com/reference/search-a-crawlbulk-job)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | yes | Bulk or crawl collection name to search. |
| `query` | query | `string` | yes | Search query to execute against the collection. |
