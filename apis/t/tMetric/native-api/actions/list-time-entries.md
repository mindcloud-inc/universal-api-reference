# List Time Entries with TMetric

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/timeentries`
- **Base URL:** `https://app.tmetric.com/api/v3`
- **Official documentation:** [List Time Entries](https://app.tmetric.com/api-docs/#/Time%20Entries/get-accounts-accountId-timeentries)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | Workspace identifier. |
| `endDate` | query | `date` | no | Filter time entries through this date. |
| `startDate` | query | `date` | no | Filter time entries from this date. |
| `userId` | query | `number` | no | Optional user identifier. |
