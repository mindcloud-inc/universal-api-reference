# Add User To Team with Runrun.it

Adds a user to a team in Runrun.it.

## Endpoint

- **Method:** `POST`
- **Path:** `/teams/:id/add_member`
- **Base URL:** `https://runrun.it/api/v1.0`
- **Official documentation:** [Add User To Team](https://runrun.it/api/documentation#teams-add-a-user-to-a-team)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Id path parameter. |
| `user_id` | body | `string` | yes | New team member id |
| `team_partnership` | body | `boolean` | no | Flag to make the new team member and other members, partners |
