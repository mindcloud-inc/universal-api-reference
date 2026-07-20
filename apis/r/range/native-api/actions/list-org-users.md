# List Org Users with Range

List organization users with optional team and relation filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/orgs/:orgId/users`
- **Base URL:** `https://api.range.co`
- **Official documentation:** [List Org Users](https://www.range.co/docs/api#rpc-list-users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `for_user_id` | query | `string` | no | Fetch users on teams this user is related to. |
| `limit` | query | `number` | no | Maximum number of users to return. |
| `org_id` | path | `string` | no | The Range organization ID. |
| `team_id` | query | `string` | no | Filter users to a specific team. |
| `user_ids` | query | `string` | no | Explicit user IDs to fetch. |
