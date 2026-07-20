# Get Profile with Bluesky

Retrieves a Bluesky profile by handle or DID.

## Endpoint

- **Method:** `GET`
- **Path:** `/xrpc/app.bsky.actor.getProfile`
- **Base URL:** `{pdsUrl}`
- **Official documentation:** [Get Profile](https://docs.bsky.app/docs/api/app-bsky-actor-get-profile)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `actor` | query | `string` | yes | Handle or DID of the profile to fetch. |
