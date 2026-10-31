# Update Project Note with Bridgit Bench

## Endpoint

- **Method:** `PATCH`
- **Path:** `/rp/api/v1/accounts/:accountId/projects/:projectId/notes/:id`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Update Project Note](https://developers.gobridgit.com/reference/projectnotes_update)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `projectId` | path | `number` | yes | The project ID the note is on |
| `id` | path | `number` | yes | The ID of the note to update |
| `message` | body | `string` | yes | — |
| `isPrivate` | body | `boolean` | no | — |
