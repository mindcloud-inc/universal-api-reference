# Get Lists with Bluesky

Retrieves Bluesky lists created by a specific account.

## Endpoint

- **Method:** `GET`
- **Path:** `/xrpc/app.bsky.graph.getLists`
- **Base URL:** `{pdsUrl}`
- **Official documentation:** [Get Lists](https://docs.bsky.app/docs/api/app-bsky-graph-get-lists)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `actor` | query | `string` | yes | Handle or DID whose lists you want to inspect. |
