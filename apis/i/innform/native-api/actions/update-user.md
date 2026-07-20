# Update User with Innform

Updates a user in Innform by ID or email.

## Endpoint

- **Method:** `PUT`
- **Path:** `/users/{idOrEmail}`
- **Base URL:** `https://api.innform.io/v1`
- **Official documentation:** [Update User](https://innform.docs.apiary.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | Updated user email. |
| `groups[]` | body | `array<string>` | no | Updated list of group names. Send multiple values as a array. |
| `idOrEmail` | path | `string` | yes | User UUID or email address. |
| `locale` | body | `string` | no | Updated user locale code. |
| `mobile` | body | `string` | no | Updated mobile number. |
| `name` | body | `string` | no | Updated user name. |
| `property` | body | `string` | no | Updated property name. |
