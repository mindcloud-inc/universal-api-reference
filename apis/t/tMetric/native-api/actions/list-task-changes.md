# List Task Changes with TMetric

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/tasks/:taskId/changes`
- **Base URL:** `https://app.tmetric.com/api/v3`
- **Official documentation:** [List Task Changes](https://app.tmetric.com/api-docs/#/Tasks/get-api-v3-accounts-accountId-tasks-taskId-changes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | Workspace identifier. |
| `taskId` | path | `number` | yes | Task identifier. |
