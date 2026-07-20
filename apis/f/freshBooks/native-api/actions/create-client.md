# Create Client with FreshBooks

Creates a new client in FreshBooks for an account.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounting/account/:accountId/users/clients`
- **Base URL:** `https://api.freshbooks.com`
- **Official documentation:** [Create Client](https://www.freshbooks.com/api/clients)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | FreshBooks accounting account ID. |
| `client.fname` | body | `string` | no | Client first name. |
| `client.lname` | body | `string` | no | Client last name. |
| `client.organization` | body | `string` | no | Client organization name. |
| `client.email` | body | `string` | no | Client email address. |
