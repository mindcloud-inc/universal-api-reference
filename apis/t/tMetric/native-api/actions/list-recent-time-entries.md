# List Recent Time Entries with TMetric

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/timeentries/recent`
- **Base URL:** `https://app.tmetric.com/api/v3`
- **Official documentation:** [List Recent Time Entries](https://app.tmetric.com/api-docs/#/Time%20Entries/get-accounts-accountId-timeentries-recent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | Workspace identifier. |
| `userId` | query | `number` | no | Optional user identifier. |
