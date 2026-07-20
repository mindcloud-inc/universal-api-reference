# List Actor Runs with Apify

Retrieves actor runs for an Apify actor.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/acts/:actorId/runs`
- **Base URL:** `https://api.apify.com`
- **Official documentation:** [List Actor Runs](https://docs.apify.com/api/v2/act-runs-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `actorId` | path | `string` | yes | The ID or username of the actor whose runs to list. |
