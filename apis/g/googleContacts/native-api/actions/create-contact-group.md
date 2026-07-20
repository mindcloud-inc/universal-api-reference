# Create Contact Group with Google Contacts

Creates a new contact group in Google Contacts.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/contactGroups`
- **Base URL:** `https://people.googleapis.com`
- **Official documentation:** [Create Contact Group](https://developers.google.com/people/api/rest/v1/contactGroups/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactGroup.name` | body | `string` | yes | Display name for the new contact group. |
| `readGroupFields` | body | `string` | no | Comma-separated fields to include in the created group response. |
