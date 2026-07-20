# Get Actor Task Input with Apify

Retrieves input for an Apify actor task.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/actor-tasks/:actorTaskId/input`
- **Base URL:** `https://api.apify.com`
- **Official documentation:** [Get Actor Task Input](https://docs.apify.com/api/v2/actor-task-input-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `actorTaskId` | path | `string` | yes | The ID of the actor task whose input to retrieve. |
