# List Task Comments with Wrike

Finds comments on a Wrike task.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks/:taskId/comments`
- **Base URL:** `https://{host}/api/v4`
- **Official documentation:** [List Task Comments](https://developers.wrike.com/api/v4/comments/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | Wrike task ID. |
