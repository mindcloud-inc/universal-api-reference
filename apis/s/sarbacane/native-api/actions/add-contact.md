# Add Contact with Sarbacane

Creates a new contact in Sarbacane.

## Endpoint

- **Method:** `POST`
- **Path:** `/lists/{listId}/contacts`
- **Base URL:** `https://api.sarbacane.com/v1`
- **Official documentation:** [Add Contact](https://developers.sarbacane.com/contacts/#add-a-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | Contact email address. |
| `listId` | path | `string` | no | Sarbacane list ID. |
| `phone` | body | `string` | no | Contact phone number. |
