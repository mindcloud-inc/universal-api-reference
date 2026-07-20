# Get Client with FreshBooks

Retrieves a client from FreshBooks for an account.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounting/account/:accountId/users/clients/:userId`
- **Base URL:** `https://api.freshbooks.com`
- **Official documentation:** [Get Client](https://www.freshbooks.com/api/clients)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | FreshBooks accounting account ID. |
| `userId` | path | `string` | yes | FreshBooks client user ID. |
