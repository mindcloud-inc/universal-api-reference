# Update User with ProfitWell

Updates a user in ProfitWell.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/users/:userIdOrUserAlias/`
- **Base URL:** `https://api.profitwell.com`
- **Official documentation:** [Update User](https://classic.paddle.com/profitwell/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userIdOrUserAlias` | path | `string` | yes | Either the user_id or the user_alias of the user. |
| `email` | body | `string` | yes | The new email address of the user. |
