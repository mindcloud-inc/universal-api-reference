# Search Actors Typeahead with Bluesky

Finds Bluesky profile suggestions by search prefix.

## Endpoint

- **Method:** `GET`
- **Path:** `/xrpc/app.bsky.actor.searchActorsTypeahead`
- **Base URL:** `{pdsUrl}`
- **Official documentation:** [Search Actors Typeahead](https://docs.bsky.app/docs/api/app-bsky-actor-search-actors-typeahead)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Search text for matching actors. |
