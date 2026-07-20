# Update User State with Range

Update a user's state fields with partial state data.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/users/:userId/state`
- **Base URL:** `https://api.range.co`
- **Official documentation:** [Update User State](https://www.range.co/docs/api#rpc-update-user-state)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `state` | body | `object` | no | Full or partial user state object. |
| `user_id` | path | `string` | no | The Range user ID. |
