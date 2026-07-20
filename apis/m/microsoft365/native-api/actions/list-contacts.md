# List Contacts with Microsoft 365

Retrieves contacts from Microsoft 365.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/me/contacts`
- **Base URL:** `https://graph.microsoft.com`
- **API:** REST (skip pagination)
- **Official documentation:** [List Contacts](https://learn.microsoft.com/en-us/graph/api/user-list-contacts?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$top` | query | `number` | no | Number of contacts to return. |
