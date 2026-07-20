# Batch Create Contacts with Google Contacts

Creates multiple new contacts in Google Contacts.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/people\:batchCreateContacts`
- **Base URL:** `https://people.googleapis.com`
- **Official documentation:** [Batch Create Contacts](https://developers.google.com/people/api/rest/v1/people/batchCreateContacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contacts[]` | body | `array<object>` | yes | Array of contacts to create. Each item should include `contactPerson` with Person fields. |
| `readMask` | body | `string` | yes | — |
| `sources[]` | body | `array<string>` | no | — |
