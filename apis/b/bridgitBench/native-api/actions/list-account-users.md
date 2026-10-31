# List Account Users with Bridgit Bench

## Endpoint

- **Method:** `GET`
- **Path:** `/rp/api/v1/accounts/:accountId/users`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [List Account Users](https://developers.gobridgit.com/reference/accountusers_query)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `group` | query | `string` | no | Optional parameter to filter results based on user groups |
| `ids` | query | `number` | no | (Optional) Filters the result to contain account users that match the ids passed in. Send multiple values as a array. |
| `nameSearch` | query | `string` | no | (Optional) Searches for users by partial name match (minimum 3 characters). |
| `search` | query | `string` | no | (Optional) Searches for users by partial match on name, email address, permission set name, or grouping name. Grouping names are only matched for active users. |
