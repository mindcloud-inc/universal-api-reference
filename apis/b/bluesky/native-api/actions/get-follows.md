# Get Follows with Bluesky

Retrieves accounts followed by a specific Bluesky account.

## Endpoint

- **Method:** `GET`
- **Path:** `/xrpc/app.bsky.graph.getFollows`
- **Base URL:** `{pdsUrl}`
- **Official documentation:** [Get Follows](https://docs.bsky.app/docs/api/app-bsky-graph-get-follows)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `actor` | query | `string` | yes | Handle or DID whose follows you want to inspect. |
