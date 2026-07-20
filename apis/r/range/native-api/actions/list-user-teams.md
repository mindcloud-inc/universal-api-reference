# List User Teams with Range

List a user's teams with optional archived and following filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/users/:userId/teams`
- **Base URL:** `https://api.range.co`
- **Official documentation:** [List User Teams](https://www.range.co/docs/api#rpc-list-teams)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include_archived` | query | `boolean` | no | Whether to include archived teams. |
| `include_following` | query | `boolean` | no | Whether to include followed teams. |
| `user_id` | path | `string` | no | The Range user ID. |
