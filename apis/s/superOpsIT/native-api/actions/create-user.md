# Create User with SuperOps IT

## Endpoint

- **Method:** `POST`
- **Path:** `/it`
- **Base URL:** `https://api.superops.ai`
- **Official documentation:** [Create User](https://developer.superops.com/it#mutation-createUser)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `firstName` | body | `string` | yes | The first name of the user. |
| `lastName` | body | `string` | no | The last name of the user. |
| `email` | body | `string` | yes | The email address used for login. |
| `contactNumber` | body | `string` | no | The contact number of the user. |
| `roleId` | body | `string` | yes | The application role ID to assign to the user. |
| `reportingManagerUserId` | body | `string` | no | The user ID of the reporting manager. |
| `departmentId` | body | `string` | no | The department ID for the user. |
| `siteId` | body | `string` | no | The site ID to associate to the user. |
