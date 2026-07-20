# Invite Project Member with Zeplin

Invites a member to a Zeplin project.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/{project_id}/members`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Invite Project Member](https://docs.zeplin.dev/reference/inviteprojectmember)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
| `handle` | body | `string` | yes | Email, username or unique identifier of the user Can also be `"me"` for joining the project as the current user |
