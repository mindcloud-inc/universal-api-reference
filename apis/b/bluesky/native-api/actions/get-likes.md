# Get Likes with Bluesky

Retrieves likes for a Bluesky post by URI.

## Endpoint

- **Method:** `GET`
- **Path:** `/xrpc/app.bsky.feed.getLikes`
- **Base URL:** `{pdsUrl}`
- **Official documentation:** [Get Likes](https://docs.bsky.app/docs/api/app-bsky-feed-get-likes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uri` | query | `string` | yes | AT-URI of the post whose likes you want to inspect. |
