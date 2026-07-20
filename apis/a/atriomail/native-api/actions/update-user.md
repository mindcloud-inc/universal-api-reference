# Update User with Atriomail

## Endpoint

- **Method:** `PUT`
- **Path:** `/users/:userId`
- **Base URL:** `https://system.atriomail.com/api/v1`
- **Official documentation:** [Update User](https://system.atriomail.com/api/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | The updated user name. |
| `userId` | path | `number` | yes | The AtrioMail user ID. |
