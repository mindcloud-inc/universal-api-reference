# Update Storm with Stormboard

Updates a Storm in Stormboard.

## Endpoint

- **Method:** `PUT`
- **Path:** `/storms/:storm_id`
- **Base URL:** `https://api.stormboard.com`
- **Official documentation:** [Update Storm](https://api.stormboard.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `avatars` | body | `string` | no | Set to 1 to show user avatars in real time, or 0 to hide them. |
| `description` | body | `string` | no | Updated storm description or goals. |
| `ideacreator` | body | `string` | no | Set to 1 to show the idea creator avatar on ideas, or 0 to hide it. |
| `storm_id` | path | `number` | yes | Storm ID from the Stormboard share dialog or related storm record. |
| `template` | body | `string` | no | Updated template ID for the storm. |
| `title` | body | `string` | no | Updated storm title. |
| `votesperuser` | body | `string` | no | Updated number of votes each user gets. |
