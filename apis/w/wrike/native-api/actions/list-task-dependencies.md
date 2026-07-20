# List Task Dependencies with Wrike

Finds dependencies for a Wrike task.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks/:taskId/dependencies`
- **Base URL:** `https://{host}/api/v4`
- **Official documentation:** [List Task Dependencies](https://developers.wrike.com/api/v4/dependencies/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | Wrike task ID. |
