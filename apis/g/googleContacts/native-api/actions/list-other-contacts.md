# List Other Contacts with Google Contacts

Retrieves other contacts from Google Contacts.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/otherContacts`
- **Base URL:** `https://people.googleapis.com`
- **Official documentation:** [List Other Contacts](https://developers.google.com/people/api/rest/v1/otherContacts/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `readMask` | query | `string` | yes | — |
| `pageSize` | query | `number` | no | — |
| `pageToken` | query | `string` | no | — |
| `requestSyncToken` | query | `boolean` | no | Whether to return next sync token on final page. |
| `syncToken` | query | `string` | no | Sync token from a previous list response. |
| `sources` | query | `string` | no | — |
