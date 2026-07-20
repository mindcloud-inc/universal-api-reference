# Update Team Member with NeetoForm

Updates an existing team member in NeetoForm.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/team_members/:team_member_id`
- **Base URL:** `https://{workspaceSubdomain}.neetoform.com/api/external/v1`
- **Official documentation:** [Update Team Member](https://apidocs.neetoform.com/api-reference/team-members/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_member_id` | path | `string` | yes | ID of the team member you want to update. |
| `email` | body | `string` | no | Email of the team member. |
| `first_name` | body | `string` | no | First name of the team member. |
| `last_name` | body | `string` | no | Last name of the team member. |
| `time_zone` | body | `string` | no | Time zone for the team member. |
| `organization_role` | body | `string` | no | Organization role for the team member. This value is case sensitive. |
