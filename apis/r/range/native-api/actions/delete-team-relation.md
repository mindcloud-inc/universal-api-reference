# Delete Team Relation with Range

Remove the relationship between a team and user.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/teams/:teamId/relations/:userId`
- **Base URL:** `https://api.range.co`
- **Official documentation:** [Delete Team Relation](https://www.range.co/docs/api#rpc-delete-team-relation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_id` | path | `string` | no | The team ID to update. |
| `user_id` | path | `string` | no | The user ID to remove from the team relation. |
