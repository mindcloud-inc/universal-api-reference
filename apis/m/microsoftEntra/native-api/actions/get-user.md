# Get User with Microsoft Entra

## Endpoint

- **Method:** `GET`
- **Path:** `/users/:userId`
- **Base URL:** `https://graph.microsoft.com/v1.0`
- **Official documentation:** [Get User](https://learn.microsoft.com/en-us/graph/api/user-get?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$select` | query | `string` | no | Comma-separated properties, such as id,displayName. |
| `userId` | path | `list<string>` | yes | — |
