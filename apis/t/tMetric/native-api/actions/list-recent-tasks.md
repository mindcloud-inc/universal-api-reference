# List Recent Tasks with TMetric

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/tasks/recent`
- **Base URL:** `https://app.tmetric.com/api/v3`
- **Official documentation:** [List Recent Tasks](https://app.tmetric.com/api-docs/#/Tasks/get-accounts-accountId-tasks-recent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | Workspace identifier. |
| `userId` | query | `number` | no | Optional user identifier. |
