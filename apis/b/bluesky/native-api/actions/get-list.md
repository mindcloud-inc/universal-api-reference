# Get List with Bluesky

Retrieves details for a specific Bluesky list.

## Endpoint

- **Method:** `GET`
- **Path:** `/xrpc/app.bsky.graph.getList`
- **Base URL:** `{pdsUrl}`
- **Official documentation:** [Get List](https://docs.bsky.app/docs/api/app-bsky-graph-get-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list` | query | `string` | yes | AT-URI of the list to inspect. |
