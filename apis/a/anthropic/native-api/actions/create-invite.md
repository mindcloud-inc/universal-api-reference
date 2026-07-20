# Create Invite with Anthropic

Creates an invite for the Anthropic organization.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/organizations/invites`
- **Base URL:** `https://api.anthropic.com`
- **Official documentation:** [Create Invite](https://platform.claude.com/docs/en/api/admin/invites/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address to invite. |
| `role` | body | `string` | yes | Organization role for the invited user. |
