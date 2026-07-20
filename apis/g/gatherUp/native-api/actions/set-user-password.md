# Set User Password with GatherUp

Updates a user password in GatherUp.

## Endpoint

- **Method:** `POST`
- **Path:** `/user/password/set`
- **Base URL:** `https://app.gatherup.com/api`
- **Official documentation:** [Set User Password](https://app.gatherup.com/api/doc/user/password/set)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `password` | body | `string` | yes | New password. |
| `userId` | body | `number` | yes | The user id. |
