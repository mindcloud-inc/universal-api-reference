# Update User Information with GatherUp

Updates an existing user in GatherUp.

## Endpoint

- **Method:** `POST`
- **Path:** `/user/manager/update`
- **Base URL:** `https://app.gatherup.com/api`
- **Official documentation:** [Update User Information](https://app.gatherup.com/api/doc/user/manager/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | User email. |
| `firstName` | body | `string` | no | User first name. |
| `lastName` | body | `string` | no | User last name. |
| `userId` | body | `number` | yes | User id. |
| `role` | body | `string` | no | User role |
