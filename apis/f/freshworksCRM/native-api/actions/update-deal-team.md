# Update Deal Team with Freshworks CRM

Updates team members for a deal in Freshworks CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/deals/:id/manage_team_members`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Update Deal Team](https://developers.freshworks.com/crm/api/#update_deal_team)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `team_users[]` | body | `array<object>` | yes |
| `team_users[].designation_id` | body | `number` | yes |
| `team_users[].user_id` | body | `number` | yes |
