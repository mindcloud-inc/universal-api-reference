# Get Lists With Membership with Bluesky

Retrieves the current account's Bluesky lists with membership for a specific actor.

## Endpoint

- **Method:** `GET`
- **Path:** `/xrpc/app.bsky.graph.getListsWithMembership`
- **Base URL:** `{pdsUrl}`
- **Official documentation:** [Get Lists With Membership](https://docs.bsky.app/docs/api/app-bsky-graph-get-lists-with-membership)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `actor` | query | `string` | yes | Handle or DID whose lists with membership you want to inspect. |
