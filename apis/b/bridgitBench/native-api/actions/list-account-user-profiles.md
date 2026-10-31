# List Account User Profiles with Bridgit Bench

## Endpoint

- **Method:** `GET`
- **Path:** `/rp/api/v1/Accounts/:id/user-profiles`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [List Account User Profiles](https://developers.gobridgit.com/reference/accounts_queryuserprofiles)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Account ID |
| `ids` | query | `number` | no | (Optional) Filters the result to contain account users that match the ids passed in. Send multiple values as a array. |
