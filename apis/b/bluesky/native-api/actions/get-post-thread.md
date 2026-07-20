# Get Post Thread with Bluesky

Retrieves a thread for a specific Bluesky post.

## Endpoint

- **Method:** `GET`
- **Path:** `/xrpc/app.bsky.feed.getPostThread`
- **Base URL:** `{pdsUrl}`
- **Official documentation:** [Get Post Thread](https://docs.bsky.app/docs/api/app-bsky-feed-get-post-thread)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uri` | query | `string` | yes | AT-URI of the post thread to load. |
