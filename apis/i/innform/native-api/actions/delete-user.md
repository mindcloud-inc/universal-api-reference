# Delete User with Innform

Deletes a user from Innform by ID or email.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/users/{idOrEmail}`
- **Base URL:** `https://api.innform.io/v1`
- **Official documentation:** [Delete User](https://innform.docs.apiary.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idOrEmail` | path | `string` | yes | User UUID or email address. |
