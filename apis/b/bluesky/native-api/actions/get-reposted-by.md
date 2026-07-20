# Get Reposted By with Bluesky

Retrieves accounts that reposted a specific Bluesky post.

## Endpoint

- **Method:** `GET`
- **Path:** `/xrpc/app.bsky.feed.getRepostedBy`
- **Base URL:** `{pdsUrl}`
- **Official documentation:** [Get Reposted By](https://docs.bsky.app/docs/api/app-bsky-feed-get-reposted-by)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uri` | query | `string` | yes | AT-URI of the post whose reposts you want to inspect. |
