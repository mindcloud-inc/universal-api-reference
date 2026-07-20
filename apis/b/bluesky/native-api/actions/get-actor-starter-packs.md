# Get Actor Starter Packs with Bluesky

Retrieves Bluesky starter packs created by a specific actor.

## Endpoint

- **Method:** `GET`
- **Path:** `/xrpc/app.bsky.graph.getActorStarterPacks`
- **Base URL:** `{pdsUrl}`
- **Official documentation:** [Get Actor Starter Packs](https://docs.bsky.app/docs/api/app-bsky-graph-get-actor-starter-packs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `actor` | query | `string` | yes | Handle or DID whose starter packs you want to inspect. |
