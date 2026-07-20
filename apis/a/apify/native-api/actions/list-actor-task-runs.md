# List Actor Task Runs with Apify

Retrieves runs for an Apify actor task.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/actor-tasks/:actorTaskId/runs`
- **Base URL:** `https://api.apify.com`
- **Official documentation:** [List Actor Task Runs](https://docs.apify.com/api/v2/actor-task-runs-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `actorTaskId` | path | `string` | yes | The ID of the actor task whose runs to list. |
