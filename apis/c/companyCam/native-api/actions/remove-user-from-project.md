# Remove User from Project with CompanyCam

Remove an assigned user from a specified Project.

## Endpoint

- **Method:** `DELETE`
- **Path:** `projects/:id/assigned_users/:userId`
- **Base URL:** `https://api.companycam.com/v2/`
- **Official documentation:** [Remove User from Project](https://docs.companycam.com/reference/removeuserfromproject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ID of the Project |
| `userId` | path | `string` | yes | — |
