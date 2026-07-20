# Create or Update Account with Journy.io

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/upsert`
- **Base URL:** `https://api.journy.io`
- **Official documentation:** [Create or Update Account](https://developers.journy.io/#operation/upsertAccount)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identification.accountId` | body | `string` | no | Unique identifier for the account in your database. |
| `identification.domain` | body | `string` | no | The domain associated with the account. |
| `properties` | body | `object` | no | Account properties to create or update. |
