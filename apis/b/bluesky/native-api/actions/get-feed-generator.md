# Get Feed Generator with Bluesky

Retrieves details for a Bluesky feed generator.

## Endpoint

- **Method:** `GET`
- **Path:** `/xrpc/app.bsky.feed.getFeedGenerator`
- **Base URL:** `{pdsUrl}`
- **Official documentation:** [Get Feed Generator](https://docs.bsky.app/docs/api/app-bsky-feed-get-feed-generator)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `feed` | query | `string` | yes | AT-URI of the feed generator to inspect. |
