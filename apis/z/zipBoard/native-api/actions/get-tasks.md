# Get Tasks with zipBoard

Retrieves tasks from zipBoard.

## Endpoint

- **Method:** `GET`
- **Path:** `/issues/tasks`
- **Base URL:** `https://app.zipboard.co/api/v1`
- **Official documentation:** [Get Tasks](https://help.zipboard.co/article/181-api-for-issues-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileid` | body | `string` | no | Optional file ID whose tasks should be fetched. |
| `priority` | body | `string` | no | Optional task priority filter. |
| `projectid` | body | `string` | no | Optional project ID whose tasks should be fetched. |
| `projectid` | query | `string` | yes | — |
| `status` | body | `string` | no | Optional task status filter. |
| `type` | body | `string` | no | Optional task type filter. |
