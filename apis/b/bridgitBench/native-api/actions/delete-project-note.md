# Delete Project Note with Bridgit Bench

## Endpoint

- **Method:** `DELETE`
- **Path:** `/rp/api/v1/accounts/:accountId/projects/:projectId/notes/:id`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Delete Project Note](https://developers.gobridgit.com/reference/projectnotes_delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `projectId` | path | `number` | yes | The project ID the note is on |
| `id` | path | `number` | yes | The ID of the note to update |
