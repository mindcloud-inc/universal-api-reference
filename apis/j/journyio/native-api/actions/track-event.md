# Track Event with Journy.io

## Endpoint

- **Method:** `POST`
- **Path:** `/track`
- **Base URL:** `https://api.journy.io`
- **Official documentation:** [Track Event](https://developers.journy.io/#operation/trackEvent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identification.account.accountId` | body | `string` | no | Unique identifier for the account in your database. |
| `identification.account.domain` | body | `string` | no | The domain associated with the account. |
| `identification.user.email` | body | `string` | no | Email address of the user. |
| `identification.user.userId` | body | `string` | no | Unique identifier for the user in your database. |
| `metadata` | body | `object` | no | Optional event metadata. |
| `name` | body | `string` | yes | Name of the event to track. |
| `triggeredAt` | body | `date` | no | Datetime when the event happened. |
