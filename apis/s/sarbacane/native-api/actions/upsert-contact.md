# Upsert Contact with Sarbacane

Finds a contact in Sarbacane, or creates one if needed.

## Endpoint

- **Method:** `POST`
- **Path:** `/lists/{listId}/contacts/upsert`
- **Base URL:** `https://api.sarbacane.com/v1`
- **Official documentation:** [Upsert Contact](https://developers.sarbacane.com/contacts/#add-edit-a-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | Contact email address. |
| `listId` | path | `string` | no | Sarbacane list ID. |
| `phone` | body | `string` | no | Contact phone number. |
