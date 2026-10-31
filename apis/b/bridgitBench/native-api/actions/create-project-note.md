# Create Project Note with Bridgit Bench

## Endpoint

- **Method:** `POST`
- **Path:** `/rp/api/v1/accounts/:accountId/projects/:projectId/notes`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Create Project Note](https://developers.gobridgit.com/reference/projectnotes_add)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `projectId` | path | `number` | yes | The project ID to add the note to |
| `message` | body | `string` | yes | — |
| `isPrivate` | body | `boolean` | yes | — |
