# Create Saved Search with Feedbin

Creates a new saved search in Feedbin.

## Endpoint

- **Method:** `POST`
- **Path:** `saved_searches.json`
- **Base URL:** `https://api.feedbin.com/v2`
- **Official documentation:** [Create Saved Search](https://github.com/feedbin/feedbin-api/blob/master/content/saved-searches.md#create-saved-search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Saved search name. |
| `query` | body | `string` | yes | Feedbin saved search query, for example javascript is:unread. |
