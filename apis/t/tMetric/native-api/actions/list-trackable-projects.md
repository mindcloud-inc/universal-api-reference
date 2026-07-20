# List Trackable Projects with TMetric

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/timeentries/projects`
- **Base URL:** `https://app.tmetric.com/api/v3`
- **Official documentation:** [List Trackable Projects](https://app.tmetric.com/api-docs/#/Time%20Entries/get-accounts-accountId-timeentries-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | Workspace identifier. |
| `userId` | query | `number` | no | Optional user identifier. |
