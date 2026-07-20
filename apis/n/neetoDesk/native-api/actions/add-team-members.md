# Add Team Members with NeetoDesk

## Endpoint

- **Method:** `POST`
- **Path:** `/team-members`
- **Base URL:** `https://{workspaceSubdomain}.neetodesk.com/api/external/v2`
- **Official documentation:** [Add Team Members](https://apidocs.neetodesk.com/api-reference/team-members/add)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails[]` | body | `array<string>` | yes | Emails of the team members to add. |
| `organization_role` | body | `string` | no | Role assigned to the new team members. |
| `invited_by` | body | `string` | no | Email of the admin sending the invitation. |
| `send_invitation_email` | body | `string` | no | Whether invitation emails should be sent. |
