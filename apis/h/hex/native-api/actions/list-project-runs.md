# List Project Runs with Hex

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{projectId}/runs`
- **Base URL:** `https://app.hex.tech/api/v1`
- **Official documentation:** [List Project Runs](https://learn.hex.tech/docs/api-integrations/api/reference#operation/GetProjectRuns)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of runs to return. |
| `offset` | query | `number` | no | Offset for paginating through project runs. |
| `projectId` | path | `string` | yes | Unique ID for a Hex project. |
| `statusFilter` | query | `string` | no | Filter runs by status. |
