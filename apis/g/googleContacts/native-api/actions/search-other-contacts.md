# Search Other Contacts with Google Contacts

Finds other contacts in Google Contacts by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/otherContacts\:search`
- **Base URL:** `https://people.googleapis.com`
- **Official documentation:** [Search Other Contacts](https://developers.google.com/people/api/rest/v1/otherContacts/search)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `query` | query | `string` | yes |
| `readMask` | query | `string` | yes |
| `pageSize` | query | `number` | no |
