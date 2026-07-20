# Get Actor Feeds with Bluesky

Retrieves Bluesky feeds created by a specific actor.

## Endpoint

- **Method:** `GET`
- **Path:** `/xrpc/app.bsky.feed.getActorFeeds`
- **Base URL:** `{pdsUrl}`
- **Official documentation:** [Get Actor Feeds](https://docs.bsky.app/docs/api/app-bsky-feed-get-actor-feeds)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `actor` | query | `string` | yes | Handle or DID whose feeds you want to inspect. |
