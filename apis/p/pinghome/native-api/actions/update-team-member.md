# Update Team Member with Pinghome

Updates an existing team member in Pinghome.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/customer-cmd/v1/team/:id/member/:memberId`
- **Base URL:** `https://api.pinghome.io`
- **Official documentation:** [Update Team Member](https://docs.pinghome.io/customer-account-management/team-organization-and-role-setup/update-team-member/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique ID of the team. |
| `memberId` | path | `string` | yes | The unique ID of the team member. |
| `role` | body | `string` | yes | The new role of the team member. |
| `new_team_id` | body | `string` | yes | The new team id for the member. |
