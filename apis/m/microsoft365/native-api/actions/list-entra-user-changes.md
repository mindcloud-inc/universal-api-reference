# List Entra User Changes with Microsoft 365

Retrieves Entra user changes from Microsoft 365.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/users/delta`
- **Base URL:** `https://graph.microsoft.com`
- **API:** REST (deltaLink pagination)
- **Official documentation:** [List Entra User Changes](https://learn.microsoft.com/en-us/graph/api/user-delta?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `$deltatoken` | query | `string` | no |
