# Get Suggested Follows By Actor with Bluesky

Retrieves Bluesky follow suggestions similar to a specific actor.

## Endpoint

- **Method:** `GET`
- **Path:** `/xrpc/app.bsky.graph.getSuggestedFollowsByActor`
- **Base URL:** `{pdsUrl}`
- **Official documentation:** [Get Suggested Follows By Actor](https://docs.bsky.app/docs/api/app-bsky-graph-get-suggested-follows-by-actor)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `actor` | query | `string` | yes | Handle or DID to use for suggested follows. |
