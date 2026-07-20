# Search Contacts with Google Contacts

Finds contacts in Google Contacts by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/people\:searchContacts`
- **Base URL:** `https://people.googleapis.com`
- **Official documentation:** [Search Contacts](https://developers.google.com/people/api/rest/v1/people/searchContacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Search text for matching contacts. |
| `readMask` | query | `string` | yes | Fields to include for each matched contact. |
| `pageSize` | query | `number` | no | — |
| `sources` | query | `string` | no | — |
