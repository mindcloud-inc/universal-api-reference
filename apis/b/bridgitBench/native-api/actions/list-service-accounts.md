# List Service Accounts with Bridgit Bench

## Endpoint

- **Method:** `GET`
- **Path:** `/rp/api/v1/accounts/:accountId/service-accounts`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [List Service Accounts](https://developers.gobridgit.com/reference/serviceaccounts_getserviceaccounts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `ids` | query | `number` | no | (Optional) Filters the result to contain accounts that match the ids passed in. Send multiple values as a array. |
