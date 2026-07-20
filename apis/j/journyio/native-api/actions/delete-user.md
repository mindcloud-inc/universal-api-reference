# Delete User with Journy.io

## Endpoint

- **Method:** `DELETE`
- **Path:** `/users`
- **Base URL:** `https://api.journy.io`
- **Official documentation:** [Delete User](https://developers.journy.io/#operation/deleteUser)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identification.email` | body | `string` | no | Email address of the user. |
| `identification.userId` | body | `string` | no | Unique identifier for the user in your database. |
