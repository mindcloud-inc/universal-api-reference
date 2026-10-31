# Delete Person Employment Period with Bridgit Bench

## Endpoint

- **Method:** `DELETE`
- **Path:** `/rp/api/v1/accounts/:accountId/persons/:personId/employment-periods/:periodId`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Delete Person Employment Period](https://developers.gobridgit.com/reference/personemploymentperiods_remove)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `personId` | path | `number` | yes | Id of the person the period belongs to |
| `periodId` | path | `number` | yes | Id of the employment period to remove |
