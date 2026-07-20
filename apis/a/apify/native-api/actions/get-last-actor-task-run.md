# Get Last Actor Task Run with Apify

Retrieves the last run for an Apify actor task.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/actor-tasks/:actorTaskId/runs/last`
- **Base URL:** `https://api.apify.com`
- **Official documentation:** [Get Last Actor Task Run](https://docs.apify.com/api/v2/actor-task-runs-last-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `actorTaskId` | path | `string` | yes | The ID of the actor task whose latest run to retrieve. |
