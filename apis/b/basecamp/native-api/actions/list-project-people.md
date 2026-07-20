# List Project People with Basecamp

Retrieves people for a project in Basecamp.

## Endpoint

- **Method:** `GET`
- **Path:** `/:accountId/projects/:projectId/people.json`
- **Base URL:** `https://3.basecampapi.com`
- **Official documentation:** [List Project People](https://github.com/basecamp/bc3-api/blob/master/sections/people.md#get-people-on-a-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | Basecamp account ID. |
| `projectId` | path | `number` | yes | Basecamp project ID. |
