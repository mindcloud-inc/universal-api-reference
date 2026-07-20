# Delete Contact with Sarbacane

Deletes an existing contact from Sarbacane.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/lists/{listId}/contacts`
- **Base URL:** `https://api.sarbacane.com/v1`
- **Official documentation:** [Delete Contact](https://developers.sarbacane.com/contacts/#delete-a-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Contact email address to remove. |
| `listId` | path | `string` | no | Sarbacane list ID. |
| `phone` | query | `string` | no | Contact phone number to remove. |
