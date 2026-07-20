# Update User with SuperOps IT

## Endpoint

- **Method:** `POST`
- **Path:** `/it`
- **Base URL:** `https://api.superops.ai`
- **Official documentation:** [Update User](https://developer.superops.com/it#mutation-updateUser)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | body | `string` | yes | The ID of the user to update. |
| `firstName` | body | `string` | no | The first name of the user. |
| `lastName` | body | `string` | no | The last name of the user. |
| `email` | body | `string` | no | The email address used for login. |
| `contactNumber` | body | `string` | no | The contact number of the user. |
| `roleId` | body | `string` | no | The application role ID to assign to the user. |
| `reportingManagerUserId` | body | `string` | no | The user ID of the reporting manager. |
| `departmentId` | body | `string` | no | The department ID for the user. |
