# Get Schedule with TMetric

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/schedule`
- **Base URL:** `https://app.tmetric.com/api/v3`
- **Official documentation:** [Get Schedule](https://app.tmetric.com/api-docs/#/Schedule/get-accounts-accountId-schedule)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | Workspace identifier. |
| `EndDate` | query | `date` | no | Schedule window end date. |
| `StartDate` | query | `date` | no | Schedule window start date. |
