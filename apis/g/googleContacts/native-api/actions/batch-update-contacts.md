# Batch Update Contacts with Google Contacts

Updates multiple contacts in Google Contacts.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/people\:batchUpdateContacts`
- **Base URL:** `https://people.googleapis.com`
- **Official documentation:** [Batch Update Contacts](https://developers.google.com/people/api/rest/v1/people/batchUpdateContacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contacts` | body | `object` | yes | Object keyed by `people/{id}`; each value is a Person patch payload (include etag). |
| `updateMask` | body | `string` | yes | — |
| `readMask` | body | `string` | no | — |
| `sources[]` | body | `array<string>` | no | — |
