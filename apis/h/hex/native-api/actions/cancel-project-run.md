# Cancel Project Run with Hex

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/:projectId/runs/:runId`
- **Base URL:** `https://app.hex.tech/api/v1`
- **Official documentation:** [Cancel Project Run](https://learn.hex.tech/docs/api-integrations/api/reference#operation/CancelRun)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Unique ID for a Hex project. |
| `runId` | path | `string` | yes | Unique ID for a Hex project run. |
