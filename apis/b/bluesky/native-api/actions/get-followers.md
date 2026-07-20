# Get Followers with Bluesky

Retrieves followers for a specific Bluesky account.

## Endpoint

- **Method:** `GET`
- **Path:** `/xrpc/app.bsky.graph.getFollowers`
- **Base URL:** `{pdsUrl}`
- **Official documentation:** [Get Followers](https://docs.bsky.app/docs/api/app-bsky-graph-get-followers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `actor` | query | `string` | yes | Handle or DID whose followers you want to inspect. |
