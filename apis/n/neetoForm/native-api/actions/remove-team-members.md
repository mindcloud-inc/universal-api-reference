# Remove Team Members with NeetoForm

## Endpoint

- **Method:** `DELETE`
- **Path:** `/team_members`
- **Base URL:** `https://{workspaceSubdomain}.neetoform.com/api/external/v1`
- **Official documentation:** [Remove Team Members](https://apidocs.neetoform.com/api-reference/team-members/remove)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails[]` | body | `array<string>` | yes | Emails of the team members to remove from the workspace. |
