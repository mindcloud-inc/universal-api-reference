# Delete Invite with Anthropic

Deletes an invite from the Anthropic organization.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/organizations/invites/{invite_id}`
- **Base URL:** `https://api.anthropic.com`
- **Official documentation:** [Delete Invite](https://platform.claude.com/docs/en/api/admin/invites/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invite_id` | path | `string` | yes | Unique ID of the invite to delete. |
