# Update Member with Ghost

Updates an existing member in Ghost.

## Endpoint

- **Method:** `PUT`
- **Path:** `/members/:id/`
- **Base URL:** `{adminDomain}/ghost/api/admin`
- **Official documentation:** [Update Member](https://docs.ghost.org/admin-api/members/updating-a-member)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Ghost member ID from the URL path. |
| `members[0].email` | body | `string` | no | Email address for the member. |
| `members[0].name` | body | `string` | no | Updated display name for the member. |
| `members[0].labels[]` | body | `array<string>` | no | Updated member labels. |
| `members[0].newsletters[]` | body | `array<string>` | no | Updated newsletters for the member. |
