# Search Posts with Bluesky

Finds Bluesky posts matching a search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/xrpc/app.bsky.feed.searchPosts`
- **Base URL:** `{pdsUrl}`
- **Official documentation:** [Search Posts](https://docs.bsky.app/docs/api/app-bsky-feed-search-posts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Search text for matching posts. |
