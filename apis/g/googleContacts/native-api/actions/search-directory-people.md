# Search Directory People with Google Contacts

Finds directory people in Google Contacts by prefix query.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/people\:searchDirectoryPeople`
- **Base URL:** `https://people.googleapis.com`
- **Official documentation:** [Search Directory People](https://developers.google.com/people/api/rest/v1/people/searchDirectoryPeople)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Prefix query string to search directory people. |
| `readMask` | query | `string` | yes | Comma-separated person fields to return. |
| `sources` | query | `string` | no | Directory source type. |
| `mergeSources` | query | `string` | no | Merge source type hint for profile merges. |
| `pageSize` | query | `number` | no | Maximum number of results to return. |
| `pageToken` | query | `string` | no | Token from previous page. |
