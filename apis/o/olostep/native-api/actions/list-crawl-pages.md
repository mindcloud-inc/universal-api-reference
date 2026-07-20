# List Crawl Pages with Olostep

Retrieves pages from an Olostep crawl.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/crawls/[:crawl_id]/pages`
- **Base URL:** `https://api.olostep.com`
- **Official documentation:** [List Crawl Pages](https://docs.olostep.com/api-reference/crawls/pages)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `crawl_id` | path | `string` | yes | The ID of the crawl whose pages you want to list. |
| `cursor` | query | `number` | no | Optional cursor index to continue listing crawl pages. |
| `search_query` | query | `string` | no | Optional search query to sort crawl pages by relevance. |
