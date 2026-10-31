# Get Project Note with Bridgit Bench

## Endpoint

- **Method:** `GET`
- **Path:** `/rp/api/v1/accounts/:accountId/projects/:projectId/notes/:id`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Get Project Note](https://developers.gobridgit.com/reference/projectnotes_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `projectId` | path | `number` | yes | The project ID the note belongs to |
| `id` | path | `number` | yes | The ID of the note |
