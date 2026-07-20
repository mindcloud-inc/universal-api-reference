# Update Saved Search with Feedbin

Updates an existing saved search in Feedbin.

## Endpoint

- **Method:** `PATCH`
- **Path:** `saved_searches/[:id].json`
- **Base URL:** `https://api.feedbin.com/v2`
- **Official documentation:** [Update Saved Search](https://github.com/feedbin/feedbin-api/blob/master/content/saved-searches.md#update-saved-search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Feedbin saved search ID. |
| `name` | body | `string` | yes | Updated saved search name. |
