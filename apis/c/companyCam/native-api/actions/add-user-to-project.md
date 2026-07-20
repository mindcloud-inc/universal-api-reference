# Add User to Project with CompanyCam

Assign a user to a project.

## Endpoint

- **Method:** `PUT`
- **Path:** `projects/:projectId/assigned_users/:userId`
- **Base URL:** `https://api.companycam.com/v2/`
- **Official documentation:** [Add User to Project](https://docs.companycam.com/reference/assignusertoproject)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | path | `string` | yes |
| `userId` | path | `string` | yes |
