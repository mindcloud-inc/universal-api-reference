# Deactivate Service Account with Bridgit Bench

## Endpoint

- **Method:** `DELETE`
- **Path:** `/rp/api/v1/accounts/:accountId/service-accounts/:id`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Deactivate Service Account](https://developers.gobridgit.com/reference/serviceaccounts_deactivateserviceaccount)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `id` | path | `number` | yes | The Service Account ID |
