# Remove User From Team with Runrun.it

Removes a user from a team in Runrun.it.

## Endpoint

- **Method:** `POST`
- **Path:** `/teams/:id/remove_member`
- **Base URL:** `https://runrun.it/api/v1.0`
- **Official documentation:** [Remove User From Team](https://runrun.it/api/documentation#teams-remove-a-user-from-team)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Id path parameter. |
| `user_id` | body | `string` | yes | Team member id |
