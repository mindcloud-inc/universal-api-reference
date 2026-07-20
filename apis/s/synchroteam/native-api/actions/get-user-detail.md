# Get User Detail with Synchroteam

Retrieves a user from Synchroteam by supported identifier.

## Endpoint

- **Method:** `GET`
- **Path:** `/Api/v2/User/Details`
- **Base URL:** `https://ws.synchroteam.com`
- **Official documentation:** [Get User Detail](https://api.synchroteam.com/v2/#get-user-detail)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifierType` | query | `string` | yes | Which identifier to use (for example: login, id). |
| `identifierValue` | query | `string` | yes | The identifier value. |
