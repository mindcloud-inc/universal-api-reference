# Search Actors with Bluesky

Finds Bluesky profiles matching a search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/xrpc/app.bsky.actor.searchActors`
- **Base URL:** `{pdsUrl}`
- **Official documentation:** [Search Actors](https://docs.bsky.app/docs/api/app-bsky-actor-search-actors)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Search text for matching actors. |
