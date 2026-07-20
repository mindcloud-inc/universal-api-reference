# List Contacts with Google Contacts

Retrieves the authenticated user's contacts from Google Contacts.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/people/me/connections`
- **Base URL:** `https://people.googleapis.com`
- **Official documentation:** [List Contacts](https://developers.google.com/people/api/rest/v1/people.connections/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `personFields` | query | `string` | yes | Comma-separated list of person fields to include in each returned contact. |
| `pageSize` | query | `number` | no | — |
| `pageToken` | query | `string` | no | — |
| `sortOrder` | query | `string` | no | — |
| `syncToken` | query | `string` | no | — |
| `requestSyncToken` | query | `boolean` | no | — |
| `sources` | query | `string` | no | Optional source types to include. |
