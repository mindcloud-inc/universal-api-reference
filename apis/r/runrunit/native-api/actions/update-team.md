# Update Team with Runrun.it

Updates an existing team in Runrun.it.

## Endpoint

- **Method:** `PUT`
- **Path:** `/teams/:id`
- **Base URL:** `https://runrun.it/api/v1.0`
- **Official documentation:** [Update Team](https://runrun.it/api/documentation#teams-update-a-team)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Id path parameter. |
| `team.name` | body | `string` | no | Name of the team |
| `team.master_user_id` | body | `string` | no | [Deprecated] Use leader_id |
| `team.cost_center` | body | `string` | no | Cost center |
