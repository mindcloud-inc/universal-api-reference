# Get Feed with Bluesky

Retrieves posts from a selected Bluesky feed.

## Endpoint

- **Method:** `GET`
- **Path:** `/xrpc/app.bsky.feed.getFeed`
- **Base URL:** `{pdsUrl}`
- **Official documentation:** [Get Feed](https://docs.bsky.app/docs/api/app-bsky-feed-get-feed)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `feed` | query | `string` | yes | AT-URI of the feed generator to read. |
