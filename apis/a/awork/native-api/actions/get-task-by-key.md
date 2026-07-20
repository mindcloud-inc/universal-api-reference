# Get Task By Key with Awork

Retrieves a task from Awork by key.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks/key/:taskIdentifier`
- **Base URL:** `https://api.awork.com/api/v1`
- **Official documentation:** [Get Task By Key](https://developers.awork.com/tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskIdentifier` | path | `string` | yes | The full task identifier combining the project key and task number, for example NIKE-42. |
