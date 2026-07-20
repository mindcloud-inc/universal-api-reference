# Update Contact Team with Freshworks CRM

Updates team members for a contact in Freshworks CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/contacts/:id/manage_team_members`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Update Contact Team](https://developers.freshworks.com/crm/api/#update_contact_team)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `team_users[]` | body | `array<object>` | yes |
| `team_users[]._destroy` | body | `boolean` | no |
| `team_users[].designation_id` | body | `number` | yes |
| `team_users[].user_id` | body | `number` | yes |
