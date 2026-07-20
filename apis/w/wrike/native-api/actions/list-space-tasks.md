# List Space Tasks with Wrike

Finds tasks in a Wrike space.

## Endpoint

- **Method:** `GET`
- **Path:** `/spaces/:spaceId/tasks`
- **Base URL:** `https://{host}/api/v4`
- **Official documentation:** [List Space Tasks](https://developers.wrike.com/api/v4/tasks/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spaceId` | path | `string` | yes | Wrike space ID. |
