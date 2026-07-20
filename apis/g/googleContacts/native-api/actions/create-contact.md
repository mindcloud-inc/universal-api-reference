# Create Contact with Google Contacts

Creates a new contact in Google Contacts.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/people\:createContact`
- **Base URL:** `https://people.googleapis.com`
- **Official documentation:** [Create Contact](https://developers.google.com/people/api/rest/v1/people/createContact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `names[]` | body | `array<object>` | yes | — |
| `emailAddresses[]` | body | `array<object>` | no | — |
| `phoneNumbers[]` | body | `array<object>` | no | — |
| `personFields` | query | `string` | yes | — |
| `sources` | query | `string` | no | Optional source types to return in post-mutate read. |
