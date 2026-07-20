# Add User with Gridfox

Adds a user to a Gridfox project.

## Endpoint

- **Method:** `POST`
- **Path:** `/users`
- **Base URL:** `https://api.gridfox.com/`
- **Official documentation:** [Add User](https://api.gridfox.com/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | Email address of the user to add to the project. |
| `groupName` | body | `string` | no | Name of the Gridfox group to assign the added user to. |
