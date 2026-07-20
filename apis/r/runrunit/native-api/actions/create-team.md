# Create Team with Runrun.it

Creates a new team in Runrun.it.

## Endpoint

- **Method:** `POST`
- **Path:** `/teams`
- **Base URL:** `https://runrun.it/api/v1.0`
- **Official documentation:** [Create Team](https://runrun.it/api/documentation#teams-create-a-team)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team.name` | body | `string` | yes | Name of the team |
| `team.master_user_id` | body | `string` | no | [Deprecated] Use leader_id |
| `team.cost_center` | body | `string` | no | Cost center |
