# Get Person Employment History with Bridgit Bench

## Endpoint

- **Method:** `GET`
- **Path:** `/rp/api/v1/accounts/:accountId/persons/:personId/employment-periods`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Get Person Employment History](https://developers.gobridgit.com/reference/personemploymentperiods_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `personId` | path | `number` | yes | Id of the person to get employment periods for |
