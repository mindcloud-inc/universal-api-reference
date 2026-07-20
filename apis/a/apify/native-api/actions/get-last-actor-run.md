# Get Last Actor Run with Apify

Retrieves the last run for an Apify actor.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/acts/:actorId/runs/last`
- **Base URL:** `https://api.apify.com`
- **Official documentation:** [Get Last Actor Run](https://docs.apify.com/api/v2/act-runs-last-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `actorId` | path | `string` | yes | The ID or username of the actor whose latest run to retrieve. |
