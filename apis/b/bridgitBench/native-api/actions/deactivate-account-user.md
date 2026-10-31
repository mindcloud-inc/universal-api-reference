# Deactivate Account User with Bridgit Bench

## Endpoint

- **Method:** `DELETE`
- **Path:** `/rp/api/v1/accounts/:accountId/users/:id`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Deactivate Account User](https://developers.gobridgit.com/reference/accountusers_delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `id` | path | `number` | yes | Id of the user to remove |
