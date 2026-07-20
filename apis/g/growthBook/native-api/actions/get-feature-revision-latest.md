# Get the most recent active draft revision with GrowthBook

Retrieves the latest draft feature revision from GrowthBook.

## Endpoint

- **Method:** `GET`
- **Path:** `/features/:id/revisions/latest`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Get the most recent active draft revision](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `mine` | query | `string` | no | If true, return only the most recent active draft authored by or contributed to by the calling user. Requires a user-scoped API key. |
