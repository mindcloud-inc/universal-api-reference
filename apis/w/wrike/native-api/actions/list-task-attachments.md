# List Task Attachments with Wrike

Finds attachments on a Wrike task.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks/:taskId/attachments`
- **Base URL:** `https://{host}/api/v4`
- **Official documentation:** [List Task Attachments](https://developers.wrike.com/api/v4/attachments/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | Wrike task ID. |
