# Get Latest Time Entry with TMetric

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/timeentries/latest`
- **Base URL:** `https://app.tmetric.com/api/v3`
- **Official documentation:** [Get Latest Time Entry](https://app.tmetric.com/api-docs/#/Time%20Entries/get-accounts-accountId-timeentries-latest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | Workspace identifier. |
| `userId` | query | `number` | no | Optional user identifier. |
