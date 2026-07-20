# Remove Users from Account with Journy.io

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/users/remove`
- **Base URL:** `https://api.journy.io`
- **Official documentation:** [Remove Users from Account](https://developers.journy.io/#operation/removeUserFromAccount)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account.accountId` | body | `string` | no | Unique identifier for the account in your database. |
| `account.domain` | body | `string` | no | The domain associated with the account. |
| `users[]` | body | `array<object>` | yes | Users to remove from the account. |
