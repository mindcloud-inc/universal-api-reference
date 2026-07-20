# Get Author Feed with Bluesky

Retrieves posts and reposts from a Bluesky actor.

## Endpoint

- **Method:** `GET`
- **Path:** `/xrpc/app.bsky.feed.getAuthorFeed`
- **Base URL:** `{pdsUrl}`
- **Official documentation:** [Get Author Feed](https://docs.bsky.app/docs/api/app-bsky-feed-get-author-feed)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `actor` | query | `string` | yes | Handle or DID whose author feed you want to inspect. |
