# Delete User with ProfitWell

Deletes a user from ProfitWell.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v2/users/:userIdOrUserAlias/`
- **Base URL:** `https://api.profitwell.com`
- **Official documentation:** [Delete User](https://classic.paddle.com/profitwell/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userIdOrUserAlias` | path | `string` | yes | Either the user_id or the user_alias of the user. |
