# Fetch Profiles with Swarm

Retrieves profiles from Swarm by profile ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/profiles/fetch`
- **Base URL:** `https://bee.theswarm.com`
- **Official documentation:** [Fetch Profiles](https://docs.theswarm.com/docs/endpoints/fetch-profile)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | body | `string` | yes | One or more Swarm profile IDs to fetch. Provide at least one ID. Send multiple values as a array. |
