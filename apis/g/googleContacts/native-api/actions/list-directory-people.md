# List Directory People with Google Contacts

Retrieves directory people from the authenticated user's domain in Google Contacts.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/people\:listDirectoryPeople`
- **Base URL:** `https://people.googleapis.com`
- **Official documentation:** [List Directory People](https://developers.google.com/people/api/rest/v1/people/listDirectoryPeople)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `readMask` | query | `string` | yes | Comma-separated person fields to return. |
| `sources` | query | `string` | no | Directory source type. |
| `mergeSources` | query | `string` | no | Merge source type hint for profile merges. |
| `pageSize` | query | `number` | no | Maximum number of directory people to return. |
| `pageToken` | query | `string` | no | Token from previous page. |
| `requestSyncToken` | query | `boolean` | no | Whether to request a sync token in the response. |
| `syncToken` | query | `string` | no | Sync token returned by a previous full sync. |
