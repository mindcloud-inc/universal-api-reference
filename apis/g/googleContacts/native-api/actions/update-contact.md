# Update Contact with Google Contacts

Updates an existing contact in Google Contacts.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/people/:resourceName:contactAction`
- **Base URL:** `https://people.googleapis.com`
- **Official documentation:** [Update Contact](https://developers.google.com/people/api/rest/v1/people/updateContact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resourceName` | path | `string` | yes | — |
| `updatePersonFields` | query | `string` | yes | — |
| `personFields` | query | `string` | no | — |
| `sources` | query | `string` | no | Optional source types to return in post-mutate read. |
| `etag` | body | `string` | yes | — |
| `names[]` | body | `array<object>` | no | — |
| `emailAddresses[]` | body | `array<object>` | no | — |
| `phoneNumbers[]` | body | `array<object>` | no | — |
