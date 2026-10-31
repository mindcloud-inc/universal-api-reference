# Create Person Employment Period with Bridgit Bench

## Endpoint

- **Method:** `POST`
- **Path:** `/rp/api/v1/accounts/:accountId/persons/:personId/employment-periods`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Create Person Employment Period](https://developers.gobridgit.com/reference/personemploymentperiods_add)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `personId` | path | `number` | yes | Id of the person to add the period to |
| `startDate` | body | `date` | yes | — |
| `endDate` | body | `date` | yes | — |
| `description` | body | `string` | no | — |
