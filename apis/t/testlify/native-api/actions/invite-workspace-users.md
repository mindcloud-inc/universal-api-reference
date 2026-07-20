# Invite Workspace Users with Testlify

Creates workspace user invitations in Testlify.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/workspace/invite/user`
- **Base URL:** `https://api.testlify.com`
- **Official documentation:** [Invite Workspace Users](https://docs.testlify.com/reference/invite_workspace_users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `members[].email` | body | `string` | yes | Email address of the invited workspace user. |
| `members[].role` | body | `string` | yes | Role to assign to the invited user. |
| `members[].userRoleId` | body | `string` | yes | Workspace user role identifier. |
