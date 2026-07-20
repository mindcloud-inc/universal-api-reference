# List Users with Verifalia

Retrieves users from Verifalia.

## Endpoint

- **Method:** `GET`
- **Path:** `/users`
- **Base URL:** `https://api-1.verifalia.com/v2.7`
- **Official documentation:** [List Users](https://verifalia.com/developers/users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sort` | query | `string` | no | Sort users by `createdOn`, `-createdOn`, `displayName`, or `-displayName`. |
| `type` | query | `string` | no | Filter users by Verifalia type: `Administrator`, `Standard`, or `BrowserApp`. |
| `includeDeleted` | query | `boolean` | no | Set to true to include deleted users in the listing. |
