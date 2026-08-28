# List Run Operations with MindCloud

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/runs/:runId/operations`
- **Base URL:** `https://connect.mindcloud.co`
- **Official documentation:** [List Run Operations](https://connect.mindcloud.co/v2/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `runId` | path | `string` | yes | Run ID for this MindCloud v2 request. |
| `where` | query | `string` | no | Optional Where query parameter documented by the MindCloud v2 API. |
