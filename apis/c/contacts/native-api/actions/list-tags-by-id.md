# List Tags by ID with Contacts+

Retrieves tags from Contacts+ by ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/tags.get`
- **Base URL:** `https://api.contactsplus.com`
- **Official documentation:** [List Tags by ID](https://www.contactsplus.com/developers/contacts-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tagIds[]` | body | `array<string>` | yes | The tag IDs to retrieve. |
| `teamId` | body | `string` | no | Retrieve tags from this team instead of personal tags. |
