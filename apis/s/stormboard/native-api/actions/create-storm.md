# Create Storm with Stormboard

Creates a Storm in Stormboard.

## Endpoint

- **Method:** `POST`
- **Path:** `/storms`
- **Base URL:** `https://api.stormboard.com`
- **Official documentation:** [Create Storm](https://api.stormboard.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `avatars` | body | `string` | no | Set to 1 to show user avatars in real time, or 0 to hide them. |
| `description` | body | `string` | no | Storm description or goals. |
| `ideacreator` | body | `string` | no | Set to 1 to show the idea creator avatar on ideas, or 0 to hide it. |
| `plan` | body | `string` | yes | Plan type for the new storm: personal, student, educator, or team. |
| `team_id` | body | `number` | no | Team ID to use when plan is team. |
| `template` | body | `number` | no | Template ID for the storm. |
| `title` | body | `string` | yes | Title of the new storm. |
| `votesperuser` | body | `number` | no | Number of votes each user gets. |
