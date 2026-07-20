# Add Time Entry Break with TMetric

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:accountId/timeentries/break`
- **Base URL:** `https://app.tmetric.com/api/v3`
- **Official documentation:** [Add Time Entry Break](https://app.tmetric.com/api-docs/#/Time%20Entries/post-accounts-accountId-timeentries-break)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | Workspace identifier. |
| `endTime` | body | `date` | no | Break end time. |
| `startTime` | body | `date` | no | Break start time. |
| `userId` | query | `number` | no | Optional user identifier. |
