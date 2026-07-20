# Add Users to Account with Journy.io

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/users/add`
- **Base URL:** `https://api.journy.io`
- **Official documentation:** [Add Users to Account](https://developers.journy.io/#operation/addUserToAccount)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account.accountId` | body | `string` | no | Unique identifier for the account in your database. |
| `account.domain` | body | `string` | no | The domain associated with the account. |
| `users[]` | body | `array<object>` | yes | Users to add to the account. |
