# Update Team Relation with Range

Update the relationship between a team and user.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/teams/:teamId/relations/:userId`
- **Base URL:** `https://api.range.co`
- **Official documentation:** [Update Team Relation](https://www.range.co/docs/api#rpc-update-team-relation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_id` | path | `string` | no | The team ID to update. |
| `user_id` | path | `string` | no | The user ID to relate to the team. |
