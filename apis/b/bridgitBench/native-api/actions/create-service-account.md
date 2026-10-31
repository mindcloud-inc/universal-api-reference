# Create Service Account with Bridgit Bench

## Endpoint

- **Method:** `POST`
- **Path:** `/rp/api/v1/accounts/:accountId/service-accounts`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Create Service Account](https://developers.gobridgit.com/reference/serviceaccounts_createserviceaccount)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `name` | body | `string` | yes | — |
| `group` | body | `string` | yes | — |
| `allowedIPNetworks[]` | body | `array<string>` | no | The list of allowed IP networks for the service account. |
