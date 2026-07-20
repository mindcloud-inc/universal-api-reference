# Get Project Insights with Currents

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/insights`
- **Base URL:** `https://api.currents.dev/v1`
- **Official documentation:** [Get Project Insights](https://docs.currents.dev/resources/api/api-resources/projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date_end` | query | `string` | yes | End date for filtering the query results |
| `date_start` | query | `string` | yes | Start date for filtering the query results |
| `projectId` | path | `string` | yes | — |
