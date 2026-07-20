# Update Team Member with Content Snare

Updates a team member in Content Snare.

## Endpoint

- **Method:** `PUT`
- **Path:** `/partner_api/v1/team_members/{id}`
- **Base URL:** `https://api.contentsnare.com`
- **Official documentation:** [Update Team Member](https://api.contentsnare.com/partner_api/v1/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Team Member ID. |
| `active` | body | `boolean` | no | Active (true) or inactive (false). It's false if user is not allowed to use the system. |
| `role` | body | `string` | no | The user’s current role |
