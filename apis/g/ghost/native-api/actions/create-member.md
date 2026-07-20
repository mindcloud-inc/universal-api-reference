# Create Member with Ghost

Creates a new member in Ghost.

## Endpoint

- **Method:** `POST`
- **Path:** `/members/`
- **Base URL:** `{adminDomain}/ghost/api/admin`
- **Official documentation:** [Create Member](https://docs.ghost.org/admin-api/members/creating-a-member)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `members[0].email` | body | `string` | yes | Email address for the member to create. |
| `members[0].name` | body | `string` | no | Display name for the member. |
| `members[0].labels[]` | body | `array<string>` | no | Optional member labels to assign. |
| `members[0].newsletters[]` | body | `array<string>` | no | Optional newsletters to subscribe the member to. |
