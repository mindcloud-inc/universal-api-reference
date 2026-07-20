# Update Team Member with NeetoDesk

## Endpoint

- **Method:** `PATCH`
- **Path:** `/team-members/:team_member_id`
- **Base URL:** `https://{workspaceSubdomain}.neetodesk.com/api/external/v2`
- **Official documentation:** [Update Team Member](https://apidocs.neetodesk.com/api-reference/team-members/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_member_id` | path | `string` | yes | Identifier of the team member. |
| `first_name` | body | `string` | no | Updated first name. |
| `last_name` | body | `string` | no | Updated last name. |
| `time_zone` | body | `string` | no | Updated time zone. |
| `organization_role` | body | `string` | no | Updated organization role. |
