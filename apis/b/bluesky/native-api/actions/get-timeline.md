# Get Timeline with Bluesky

Retrieves the current account's Bluesky home timeline.

## Endpoint

- **Method:** `GET`
- **Path:** `/xrpc/app.bsky.feed.getTimeline`
- **Base URL:** `{pdsUrl}`
- **Official documentation:** [Get Timeline](https://docs.bsky.app/docs/api/app-bsky-feed-get-timeline)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of timeline entries to return. |
| `cursor` | query | `string` | no | Cursor for the next page of timeline results. |
