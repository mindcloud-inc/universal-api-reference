# List Projects with Meisterplan

Retrieves a list of projects from Meisterplan.

## Endpoint

- **Method:** `GET`
- **Path:** `/scenarios/:scenarioId/projects`
- **Base URL:** `https://api.us.meisterplan.com/v1`
- **Official documentation:** [List Projects](https://api.us.meisterplan.com/docs/api.html#operation/GetAllProjects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scenarioId` | path | `string` | yes | Internal Meisterplan scenario identifier. |
| `pageSize` | query | `number` | no | Number of results to return. |
| `pageAfter` | query | `string` | no | Cursor after which to retrieve results. |
| `filter` | query | `string` | no | Stringified JSON filter object. |
