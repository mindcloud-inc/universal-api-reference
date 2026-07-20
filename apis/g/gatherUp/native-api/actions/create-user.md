# Create User with GatherUp

Creates a new user in GatherUp.

## Endpoint

- **Method:** `POST`
- **Path:** `/user/create`
- **Base URL:** `https://app.gatherup.com/api`
- **Official documentation:** [Create User](https://app.gatherup.com/api/doc/user/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | User email. |
| `firstName` | body | `string` | yes | User first name. |
| `lastName` | body | `string` | yes | User last name. |
| `roleId` | body | `number` | no | Role Permission ID, where: 3 = Manager 4 = Team (Default) 5 = Contributor 6 = Read Only Administrators and Agency Manager can not be created via API. |
| `sendPasswordEmail` | body | `boolean` | no | Send email with password |
| `businessId{N}` | body | `number` | no | Managed business id. |
