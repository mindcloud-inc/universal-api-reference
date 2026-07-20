# Update User with Time Doctor

Updates an existing user in Time Doctor.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/1.0/users/:userId`
- **Base URL:** `https://api2.timedoctor.com`
- **Official documentation:** [Update User](https://api2.timedoctor.com/#operation/putUser)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | ID of the user to update. |
| `name` | body | `string` | no | User alias in the company. |
| `role` | body | `string` | no | User role in the company. |
