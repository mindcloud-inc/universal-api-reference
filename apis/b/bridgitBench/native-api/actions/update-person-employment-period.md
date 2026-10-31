# Update Person Employment Period with Bridgit Bench

## Endpoint

- **Method:** `PATCH`
- **Path:** `/rp/api/v1/accounts/:accountId/persons/:personId/employment-periods/:periodId`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Update Person Employment Period](https://developers.gobridgit.com/reference/personemploymentperiods_update)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `personId` | path | `number` | yes | Id of the person the period belongs to |
| `periodId` | path | `number` | yes | Id of the employment period to update |
| `startDate` | body | `date` | no | — |
| `endDate` | body | `date` | no | — |
| `description` | body | `string` | no | An empty string clears the description. |
