# Get Starter Pack with Bluesky

Retrieves details for a specific Bluesky starter pack.

## Endpoint

- **Method:** `GET`
- **Path:** `/xrpc/app.bsky.graph.getStarterPack`
- **Base URL:** `{pdsUrl}`
- **Official documentation:** [Get Starter Pack](https://docs.bsky.app/docs/api/app-bsky-graph-get-starter-pack)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `starterPack` | query | `string` | yes | AT-URI of the starter pack to inspect. |
