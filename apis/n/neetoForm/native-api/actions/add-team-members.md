# Add Team Members with NeetoForm

Adds team members to a NeetoForm workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/team_members`
- **Base URL:** `https://{workspaceSubdomain}.neetoform.com/api/external/v1`
- **Official documentation:** [Add Team Members](https://apidocs.neetoform.com/api-reference/team-members/add)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_role` | body | `string` | no | Role assigned to the new team members in the workspace. |
| `emails[]` | body | `array<string>` | yes | Emails of the team members to add to the workspace. |
| `invited_by` | body | `string` | no | Email of the admin sending the invitation. |
| `send_invitation_email` | body | `string` | no | Set to false to skip sending invitation emails. |
