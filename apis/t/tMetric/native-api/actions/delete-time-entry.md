# Delete Time Entry with TMetric

## Endpoint

- **Method:** `DELETE`
- **Path:** `/accounts/:accountId/timeentries/:timeEntryId`
- **Base URL:** `https://app.tmetric.com/api/v3`
- **Official documentation:** [Delete Time Entry](https://app.tmetric.com/api-docs/#/Time%20Entries/delete-accounts-accountId-timeentries-timeEntryId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | Workspace identifier. |
| `timeEntryId` | path | `number` | yes | Time entry identifier. |
