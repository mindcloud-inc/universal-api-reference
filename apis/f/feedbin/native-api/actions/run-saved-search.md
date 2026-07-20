# Run Saved Search with Feedbin

Retrieves saved search results from Feedbin.

## Endpoint

- **Method:** `GET`
- **Path:** `saved_searches/[:id].json`
- **Base URL:** `https://api.feedbin.com/v2`
- **Official documentation:** [Run Saved Search](https://github.com/feedbin/feedbin-api/blob/master/content/saved-searches.md#get-saved-search)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Feedbin saved search ID. |
| `include_entries` | query | `boolean` | no | Return matching entry objects instead of entry IDs. |
