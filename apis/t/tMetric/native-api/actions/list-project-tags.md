# List Project Tags with TMetric

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/timeentries/tags`
- **Base URL:** `https://app.tmetric.com/api/v3`
- **Official documentation:** [List Project Tags](https://app.tmetric.com/api-docs/#/Time%20Entries/get-accounts-accountId-timeentries-tags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | Workspace identifier. |
| `projectId` | query | `number` | no | Project identifier. |
