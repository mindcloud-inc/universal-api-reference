# Get User with Splitwise

Retrieves another user's details from Splitwise.

## Endpoint

- **Method:** `GET`
- **Path:** `/get_user/[:id]`
- **Base URL:** `https://secure.splitwise.com/api/v3.0`
- **Official documentation:** [Get User](https://dev.splitwise.com/#tag/users/paths/~1get_user~1{id}/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Splitwise user ID to retrieve. |
