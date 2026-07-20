# Get Quotes with Bluesky

Retrieves quote posts for a specific Bluesky post.

## Endpoint

- **Method:** `GET`
- **Path:** `/xrpc/app.bsky.feed.getQuotes`
- **Base URL:** `{pdsUrl}`
- **Official documentation:** [Get Quotes](https://docs.bsky.app/docs/api/app-bsky-feed-get-quotes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uri` | query | `string` | yes | AT-URI of the post whose quotes you want to inspect. |
