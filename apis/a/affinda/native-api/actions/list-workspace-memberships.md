# Get list of all workspace memberships with Affinda

Retrieves all workspace memberships from Affinda.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/workspace_memberships`
- **Base URL:** `https://api.us1.affinda.com`
- **Official documentation:** [Get list of all workspace memberships](https://docs.affinda.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `string` | no | The numbers of results to return. |
| `offset` | query | `string` | no | The number of documents to skip before starting to collect the result set. |
| `user` | query | `string` | no | Partial text match on user's email, case-insensitive. |
| `workspace` | query | `string` | no | Filter by workspace. |
