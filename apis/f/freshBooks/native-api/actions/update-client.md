# Update Client with FreshBooks

Updates an existing client in FreshBooks for an account.

## Endpoint

- **Method:** `PUT`
- **Path:** `/accounting/account/:accountId/users/clients/:userId`
- **Base URL:** `https://api.freshbooks.com`
- **Official documentation:** [Update Client](https://www.freshbooks.com/api/clients)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | FreshBooks accounting account ID. |
| `userId` | path | `string` | yes | FreshBooks client user ID. |
| `client.fname` | body | `string` | no | Client first name. |
| `client.lname` | body | `string` | no | Client last name. |
| `client.organization` | body | `string` | no | Client organization name. |
| `client.email` | body | `string` | no | Client email address. |
