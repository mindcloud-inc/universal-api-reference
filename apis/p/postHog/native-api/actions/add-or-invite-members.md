# Add or Invite Members with PostHog

Creates an organization invite in PostHog.

## Endpoint

- **Method:** `POST`
- **Path:** `/organizations/:organizationId/invites/`
- **Base URL:** `https://us.posthog.com/api`
- **Official documentation:** [Add or Invite Members](https://posthog.com/docs/api/invites)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | UUID of the organization. |
| `target_email` | body | `string` | yes | Email address to invite. |
| `first_name` | body | `string` | no | First name of the invited user. |
| `level` | body | `list<number>` | no | Organization membership level (1 member, 8 administrator, 15 owner). Accepted values: `1`, `15`, `8`. |
| `private_project_access[]` | body | `array<object>` | no | List of private project access entries (team/project IDs with access levels). |
| `message` | body | `string` | no | Optional invitation message. |
| `send_email` | body | `boolean` | no | Whether to send the invite email. |
| `combine_pending_invites` | body | `boolean` | no | Whether to combine with existing pending invites for the same email. |
