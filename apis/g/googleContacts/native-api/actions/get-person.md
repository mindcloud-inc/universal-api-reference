# Get Person with Google Contacts

Retrieves a person from Google Contacts.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/people/:resourceName`
- **Base URL:** `https://people.googleapis.com`
- **Official documentation:** [Get Person](https://developers.google.com/people/api/rest/v1/people/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resourceName` | path | `string` | yes | Person ID segment (use `me` or a contact ID like `c123`, not `people/...`). |
| `personFields` | query | `string` | yes | Comma-separated person fields to include. |
| `sources` | query | `string` | no | — |
