# Reset Service Account Password with Bridgit Bench

## Endpoint

- **Method:** `POST`
- **Path:** `/rp/api/v1/accounts/:accountId/service-accounts/:id/reset-password`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Reset Service Account Password](https://developers.gobridgit.com/reference/serviceaccounts_resetpassword)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `id` | path | `number` | yes | The Service Account ID |
