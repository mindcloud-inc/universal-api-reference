# Get User with Innform

Retrieves a user from Innform by ID or email.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/{idOrEmail}`
- **Base URL:** `https://api.innform.io/v1`
- **Official documentation:** [Get User](https://innform.docs.apiary.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idOrEmail` | path | `string` | yes | User UUID or email address. |
