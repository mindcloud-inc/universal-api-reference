# Get Subscription History For User with ProfitWell

Retrieves subscription history for a user from ProfitWell.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/users/:userIdOrUserAlias/`
- **Base URL:** `https://api.profitwell.com`
- **Official documentation:** [Get Subscription History For User](https://classic.paddle.com/profitwell/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userIdOrUserAlias` | path | `string` | yes | Either the user_id or the user_alias of the user. |
