# Attach File to Task Comment with Jostle

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/tasks/task/:taskId/comment/:commentId/attachment`
- **Base URL:** `https://api-prod.jostle.us`
- **Official documentation:** [Attach File to Task Comment](https://api.jostle.me/reference/commentattachment-1)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | Id of the targeted task |
| `commentId` | path | `string` | yes | Id of the targeted task comment |
| `url` | body | `string` | yes | URL pointing to a file to upload |
