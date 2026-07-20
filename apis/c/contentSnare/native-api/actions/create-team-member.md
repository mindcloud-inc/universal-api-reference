# Create Team Member with Content Snare

Creates a team member in Content Snare.

## Endpoint

- **Method:** `POST`
- **Path:** `/partner_api/v1/team_members`
- **Base URL:** `https://api.contentsnare.com`
- **Official documentation:** [Create Team Member](https://api.contentsnare.com/partner_api/v1/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Contact email address |
| `full_name` | body | `string` | yes | Contact full name |
| `personal_message` | body | `string` | no | The message is included in the invitation email |
| `phone` | body | `string` | no | Phone number |
| `role` | body | `string` | yes | The user’s current role |
