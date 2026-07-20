# Delete Account with Journy.io

## Endpoint

- **Method:** `DELETE`
- **Path:** `/accounts`
- **Base URL:** `https://api.journy.io`
- **Official documentation:** [Delete Account](https://developers.journy.io/#operation/deleteAccount)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identification.accountId` | body | `string` | no | Unique identifier for the account in your database. |
| `identification.domain` | body | `string` | no | The domain associated with the account. |
