# Remove Team Members with NeetoInvoice

Removes selected team members from NeetoInvoice.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/team_members`
- **Base URL:** `https://{workspaceSubdomain}.neetoinvoice.com/api/external/v1`
- **Official documentation:** [Remove Team Members](https://apidocs.neetoinvoice.com/api-reference/team-members/remove)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_member_ids` | body | `string` | no | Team member identifiers to remove. |
