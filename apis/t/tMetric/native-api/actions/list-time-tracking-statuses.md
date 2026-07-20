# List Time Tracking Statuses with TMetric

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/timeentries/statuses`
- **Base URL:** `https://app.tmetric.com/api/v3`
- **Official documentation:** [List Time Tracking Statuses](https://app.tmetric.com/api-docs/#/Time%20Entries/get-accounts-accountId-timeentries-statuses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | Workspace identifier. |
| `teamId` | query | `number` | no | Optional team identifier. |
