# Get List Feed with Bluesky

Retrieves recent posts from a Bluesky list.

## Endpoint

- **Method:** `GET`
- **Path:** `/xrpc/app.bsky.feed.getListFeed`
- **Base URL:** `{pdsUrl}`
- **Official documentation:** [Get List Feed](https://docs.bsky.app/docs/api/app-bsky-feed-get-list-feed)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list` | query | `string` | yes | AT-URI of the list whose feed you want to read. |
