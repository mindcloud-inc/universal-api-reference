# Get Actor Run with Apify

Retrieves an actor run from Apify.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/acts/:actorId/runs/:runId`
- **Base URL:** `https://api.apify.com`
- **Official documentation:** [Get Actor Run](https://docs.apify.com/api/v2/act-run-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `actorId` | path | `string` | yes | The ID or username of the actor that owns the run. |
| `runId` | path | `string` | yes | The ID of the actor run to retrieve. |
