# Update User Group with Gridfox

Updates a user's group in a Gridfox project.

## Endpoint

- **Method:** `PUT`
- **Path:** `/users/:userId`
- **Base URL:** `https://api.gridfox.com/`
- **Official documentation:** [Update User Group](https://api.gridfox.com/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupName` | body | `string` | no | Name of the Gridfox group to assign the user to. |
| `userId` | path | `string` | no | Numeric Gridfox user ID from the path parameter. |
