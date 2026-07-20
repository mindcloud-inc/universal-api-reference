# Get Project with Basecamp

Retrieves a project from Basecamp.

## Endpoint

- **Method:** `GET`
- **Path:** `/:accountId/projects/:projectId.json`
- **Base URL:** `https://3.basecampapi.com`
- **Official documentation:** [Get Project](https://github.com/basecamp/bc3-api/blob/master/sections/projects.md#get-a-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | Basecamp account ID. |
| `projectId` | path | `number` | yes | Basecamp project ID. |
