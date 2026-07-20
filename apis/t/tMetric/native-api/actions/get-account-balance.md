# Get Account Balance with TMetric

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/balance`
- **Base URL:** `https://app.tmetric.com/api/v3`
- **Official documentation:** [Get Account Balance](https://app.tmetric.com/api-docs/#/Time%20Balance/get-accounts-accountId-balance)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | Workspace identifier. |
| `userId` | query | `number` | no | Optional user identifier. |
