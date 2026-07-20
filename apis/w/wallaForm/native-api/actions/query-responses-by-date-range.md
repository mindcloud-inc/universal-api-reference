# Query Responses by Date Range with Walla Form

## Endpoint

- **Method:** `GET`
- **Path:** `/workspace/:workspaceKey/project/:projectKey/response/query/dateRange`
- **Base URL:** `https://walla-api.data-lab.workers.dev`
- **Official documentation:** [Query Responses by Date Range](https://walla-api.data-lab.workers.dev/ui)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceKey` | path | `string` | yes | The Walla workspace key. |
| `projectKey` | path | `string` | yes | The Walla project key. |
| `startDate` | query | `date` | yes | The start of the date range, in ISO 8601 format. |
| `endDate` | query | `date` | yes | The end of the date range, in ISO 8601 format. |
