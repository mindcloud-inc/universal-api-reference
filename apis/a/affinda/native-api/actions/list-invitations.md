# Get list of all invitations with Affinda

Retrieves all accessible invitations from Affinda.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/invitations`
- **Base URL:** `https://api.us1.affinda.com`
- **Official documentation:** [Get list of all invitations](https://docs.affinda.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `string` | no | The numbers of results to return. |
| `offset` | query | `string` | no | The number of documents to skip before starting to collect the result set. |
| `organization` | query | `string` | no | Filter by organization. |
| `role` | query | `string` | no | Filter by role. |
| `status` | query | `string` | no | Filter by status. |
